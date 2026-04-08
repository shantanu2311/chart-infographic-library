---
title: Bubble Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: bubble-chart
library: d3
---

# Bubble Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Bubble Chart — D3.js v7 Starter
// Data format: [{ x: number, y: number, size: number, label: string, category: string }]

import * as d3 from "d3";

const data = [
  { x: 120, y: 8.2, size: 500, label: "Plant A", category: "EAF" },
  { x: 85, y: 4.5, size: 200, label: "Plant B", category: "Induction" },
  { x: 200, y: 12.5, size: 800, label: "Plant C", category: "EAF" },
  { x: 150, y: 9.8, size: 350, label: "Plant D", category: "Re-rolling" },
  { x: 60, y: 3.2, size: 150, label: "Plant E", category: "Induction" },
  { x: 180, y: 11.0, size: 600, label: "Plant F", category: "EAF" },
  { x: 95, y: 6.3, size: 280, label: "Plant G", category: "Re-rolling" },
];

const margin = { top: 20, right: 120, bottom: 50, left: 60 };
const width = 700 - margin.left - margin.right;
const height = 450 - margin.top - margin.bottom;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales
const x = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.x) * 1.1])
  .range([0, width]);

const y = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.y) * 1.1])
  .range([height, 0]);

const r = d3.scaleSqrt()
  .domain([0, d3.max(data, (d) => d.size)])
  .range([4, 40]);

const color = d3.scaleOrdinal()
  .domain(["EAF", "Induction", "Re-rolling"])
  .range(["#e63946", "#457b9d", "#2a9d8f"]);

// Axes
svg.append("g").attr("transform", `translate(0,${height})`).call(d3.axisBottom(x));
svg.append("g").call(d3.axisLeft(y));

// Axis labels
svg.append("text")
  .attr("x", width / 2).attr("y", height + 40)
  .attr("text-anchor", "middle").style("font-size", "13px")
  .text("Production (tonnes/month)");

svg.append("text")
  .attr("transform", "rotate(-90)")
  .attr("x", -height / 2).attr("y", -45)
  .attr("text-anchor", "middle").style("font-size", "13px")
  .text("Emissions (tCO2e)");

// Bubbles
svg.selectAll("circle")
  .data(data)
  .join("circle")
  .attr("cx", (d) => x(d.x))
  .attr("cy", (d) => y(d.y))
  .attr("r", (d) => r(d.size))
  .attr("fill", (d) => color(d.category))
  .attr("opacity", 0.7)
  .attr("stroke", (d) => color(d.category))
  .attr("stroke-width", 1.5);

// Labels inside large bubbles
svg.selectAll(".bubble-label")
  .data(data.filter((d) => r(d.size) > 15))
  .join("text")
  .attr("class", "bubble-label")
  .attr("x", (d) => x(d.x))
  .attr("y", (d) => y(d.y))
  .attr("text-anchor", "middle")
  .attr("dy", "0.35em")
  .style("font-size", "10px")
  .style("fill", "#fff")
  .text((d) => d.label);
```

## Configuration Options
- `r` scale — `d3.scaleSqrt()` ensures area is proportional (not radius)
- `opacity` — lower for overlapping bubbles, higher for sparse data
- Maximum bubble size — adjust `.range([4, 40])` upper bound
- `stroke` — matching or contrasting border color

## Energy/Climate Data Example
```javascript
// Plants: production vs emissions, bubble size = energy consumption (GJ)
const data = [
  { x: 120, y: 8.2, size: 500, label: "EAF-1", category: "EAF" },
  { x: 85, y: 4.5, size: 200, label: "IF-1", category: "Induction" },
  { x: 200, y: 12.5, size: 800, label: "EAF-2", category: "EAF" },
];
```

## Customization Tips
- Add size legend showing reference circles at key values
- Use `d3.forceSimulation()` for packed bubble layout (no x/y axes)
- Add zoom with `d3.zoom()` for dense clusters
- Tooltip on hover: show all three encoded values (x, y, size)

## Related
- [[Bubble Chart]] — chart type reference
- [[Bubble Chart — Plotly Template]] — Plotly alternative
