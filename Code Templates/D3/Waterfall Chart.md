---
title: Waterfall Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: waterfall-chart
library: d3
---

# Waterfall Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Waterfall Chart — D3.js v7 Starter
// Data format: [{ label: string, value: number, type: "increase"|"decrease"|"total" }]

import * as d3 from "d3";

const rawData = [
  { label: "Baseline", value: 10000, type: "total" },
  { label: "Energy Eff.", value: -1200, type: "decrease" },
  { label: "Solar PV", value: -1800, type: "decrease" },
  { label: "Fuel Switch", value: -800, type: "decrease" },
  { label: "Process Opt.", value: -500, type: "decrease" },
  { label: "Prod. Increase", value: 600, type: "increase" },
  { label: "Net Emissions", value: 0, type: "total" }, // auto-calculated
];

// Calculate cumulative positions
let cumulative = 0;
const data = rawData.map((d) => {
  if (d.type === "total" && d.label === "Baseline") {
    cumulative = d.value;
    return { ...d, start: 0, end: d.value };
  }
  if (d.type === "total") {
    return { ...d, start: 0, end: cumulative, value: cumulative };
  }
  const start = cumulative;
  cumulative += d.value;
  return { ...d, start: Math.min(start, cumulative), end: Math.max(start, cumulative) };
});

const margin = { top: 20, right: 30, bottom: 60, left: 70 };
const width = 700 - margin.left - margin.right;
const height = 400 - margin.top - margin.bottom;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales
const x = d3.scaleBand()
  .domain(data.map((d) => d.label))
  .range([0, width])
  .padding(0.3);

const y = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.end) * 1.08])
  .range([height, 0]);

const colorMap = { total: "#457b9d", increase: "#e63946", decrease: "#2a9d8f" };

// Axes
svg.append("g")
  .attr("transform", `translate(0,${height})`)
  .call(d3.axisBottom(x))
  .selectAll("text")
  .attr("transform", "rotate(-25)")
  .attr("text-anchor", "end");

svg.append("g").call(d3.axisLeft(y));

// Bars
svg.selectAll("rect")
  .data(data)
  .join("rect")
  .attr("x", (d) => x(d.label))
  .attr("y", (d) => y(d.end))
  .attr("width", x.bandwidth())
  .attr("height", (d) => y(d.start) - y(d.end))
  .attr("fill", (d) => colorMap[d.type])
  .attr("rx", 2);

// Connector lines between bars
data.forEach((d, i) => {
  if (i < data.length - 1 && d.type !== "total") {
    svg.append("line")
      .attr("x1", x(d.label) + x.bandwidth())
      .attr("x2", x(data[i + 1].label))
      .attr("y1", y(cumulative <= d.end ? d.start + d.value : d.start))
      .attr("y2", y(cumulative <= d.end ? d.start + d.value : d.start))
      .attr("stroke", "#999")
      .attr("stroke-dasharray", "3,3");
  }
});

// Value labels
svg.selectAll(".val-label")
  .data(data)
  .join("text")
  .attr("class", "val-label")
  .attr("x", (d) => x(d.label) + x.bandwidth() / 2)
  .attr("y", (d) => y(d.end) - 6)
  .attr("text-anchor", "middle")
  .style("font-size", "11px")
  .text((d) => (d.type === "total" ? d.end : d.value));
```

## Configuration Options
- `colorMap` — customize colors for increase, decrease, and total bars
- `padding` — bar spacing (0 to 1)
- Connector lines — dashed lines between bars showing running total
- `domain` max — multiply by 1.08 for headroom above tallest bar

## Energy/Climate Data Example
```javascript
// Emission reduction waterfall (tCO2e/year)
const rawData = [
  { label: "Current", value: 10000, type: "total" },
  { label: "VFD Motors", value: -1200, type: "decrease" },
  { label: "Rooftop Solar", value: -1800, type: "decrease" },
  { label: "PNG Switch", value: -800, type: "decrease" },
  { label: "Waste Heat Recovery", value: -500, type: "decrease" },
  { label: "Target", value: 0, type: "total" },
];
```

## Customization Tips
- Auto-calculate the final total: `cumulative` after processing all items
- Add animation: transition bars growing from the connector line position
- Color negative as green (reduction) and positive as red (increase) for emissions context
- Add a horizontal reference line for a target value

## Related
- [[Waterfall Chart]] — chart type reference
- [[Waterfall Chart — Plotly Template]] — Plotly alternative
