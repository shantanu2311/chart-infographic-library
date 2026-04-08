---
title: Scatter Plot — D3.js Template
tags:
  - code-template
  - d3
chart_type: scatter-plot
library: d3
---

# Scatter Plot — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Scatter Plot — D3.js v7 Starter
// Data format: [{ x: number, y: number, category: string }]

import * as d3 from "d3";

const data = [
  { x: 120, y: 8.2, category: "EAF" },
  { x: 85, y: 6.1, category: "Induction" },
  { x: 200, y: 12.5, category: "EAF" },
  { x: 150, y: 9.8, category: "Re-rolling" },
  { x: 60, y: 4.3, category: "Induction" },
  { x: 180, y: 11.0, category: "EAF" },
  { x: 95, y: 7.2, category: "Re-rolling" },
  { x: 110, y: 7.9, category: "Induction" },
  { x: 250, y: 15.1, category: "EAF" },
  { x: 70, y: 5.5, category: "Re-rolling" },
];

const margin = { top: 20, right: 120, bottom: 50, left: 60 };
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
const x = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.x) * 1.1])
  .range([0, width]);

const y = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.y) * 1.1])
  .range([height, 0]);

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
  .text("Production (tonnes)");

svg.append("text")
  .attr("transform", "rotate(-90)")
  .attr("x", -height / 2).attr("y", -45)
  .attr("text-anchor", "middle").style("font-size", "13px")
  .text("Emissions (tCO2e)");

// Points
svg.selectAll("circle")
  .data(data)
  .join("circle")
  .attr("cx", (d) => x(d.x))
  .attr("cy", (d) => y(d.y))
  .attr("r", 6)
  .attr("fill", (d) => color(d.category))
  .attr("opacity", 0.8)
  .attr("stroke", "#fff")
  .attr("stroke-width", 1);

// Legend
const categories = ["EAF", "Induction", "Re-rolling"];
categories.forEach((cat, i) => {
  const g = svg.append("g").attr("transform", `translate(${width + 15}, ${i * 22})`);
  g.append("circle").attr("cx", 7).attr("cy", 7).attr("r", 6).attr("fill", color(cat));
  g.append("text").attr("x", 18).attr("y", 11).text(cat).style("font-size", "12px");
});
```

## Configuration Options
- `r` — point radius; map to a data variable for bubble chart effect
- `color` scale — use `d3.scaleOrdinal(d3.schemeTableau10)` for auto palettes
- `opacity` — lower to handle overlapping points
- Add `.on("mouseover", ...)` for hover tooltips

## Energy/Climate Data Example
```javascript
// Steel plants: production vs emissions by process type
const data = [
  { x: 120, y: 8.2, category: "EAF" },
  { x: 200, y: 12.5, category: "EAF" },
  { x: 85, y: 6.1, category: "Induction Furnace" },
  { x: 150, y: 9.8, category: "Re-rolling Mill" },
];
```

## Customization Tips
- Add a trend line with `d3.line()` using a regression calculation
- Use `d3.brush()` to enable brushing/selection for filtering
- Encode a third variable as point radius for a bubble chart
- Add Voronoi overlay for easier hover targeting on dense plots

## Related
- [[Scatter Plot]] — chart type reference
- [[Scatter Plot — Plotly Template]] — Plotly alternative
