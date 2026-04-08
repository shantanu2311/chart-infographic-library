---
title: Bar Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: bar-chart
library: d3
---

# Bar Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Bar Chart — D3.js v7 Starter
// Data format: [{ label: string, value: number }]

import * as d3 from "d3";

const data = [
  { label: "Coal", value: 450 },
  { label: "Natural Gas", value: 320 },
  { label: "Solar", value: 180 },
  { label: "Wind", value: 210 },
  { label: "Hydro", value: 160 },
  { label: "Nuclear", value: 280 },
];

// Dimensions
const margin = { top: 20, right: 30, bottom: 40, left: 120 };
const width = 700 - margin.left - margin.right;
const height = 400 - margin.top - margin.bottom;

// Create responsive SVG
const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales — horizontal bars with categorical y-axis
const x = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.value)])
  .range([0, width]);

const y = d3.scaleBand()
  .domain(data.map((d) => d.label))
  .range([0, height])
  .padding(0.2);

// Axes
svg.append("g").call(d3.axisLeft(y));
svg.append("g")
  .attr("transform", `translate(0,${height})`)
  .call(d3.axisBottom(x).ticks(6));

// Bars
svg.selectAll("rect")
  .data(data)
  .join("rect")
  .attr("y", (d) => y(d.label))
  .attr("x", 0)
  .attr("width", (d) => x(d.value))
  .attr("height", y.bandwidth())
  .attr("fill", "#4f86c6")
  .attr("rx", 3);

// Value labels
svg.selectAll(".label")
  .data(data)
  .join("text")
  .attr("class", "label")
  .attr("x", (d) => x(d.value) + 5)
  .attr("y", (d) => y(d.label) + y.bandwidth() / 2)
  .attr("dy", "0.35em")
  .text((d) => d.value)
  .style("font-size", "12px")
  .style("fill", "#333");
```

## Configuration Options
- `margin` — adjust spacing for longer labels on the y-axis
- `y.padding()` — controls gap between bars (0 to 1)
- `fill` — change bar color; use a `d3.scaleOrdinal()` for category colors
- `rx` — border radius on bar corners

## Energy/Climate Data Example
```javascript
// Electricity generation by source (TWh)
const data = [
  { label: "Coal", value: 1042 },
  { label: "Gas", value: 68 },
  { label: "Solar", value: 113 },
  { label: "Wind", value: 82 },
  { label: "Hydro", value: 162 },
  { label: "Nuclear", value: 47 },
  { label: "Biomass", value: 53 },
];
```

## Customization Tips
- Sort data with `data.sort((a, b) => b.value - a.value)` for ranked bars
- Add transitions: `.transition().duration(600).attr("width", d => x(d.value))`
- For vertical bars, swap x/y scales and use `scaleBand` on x-axis
- Add tooltips with a `div` overlay on `mouseover` events

## Related
- [[Bar Chart]] — chart type reference
- [[Bar Chart — Plotly Template]] — Plotly alternative
