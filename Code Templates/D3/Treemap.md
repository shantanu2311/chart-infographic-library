---
title: Treemap — D3.js Template
tags:
  - code-template
  - d3
chart_type: treemap
library: d3
---

# Treemap — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Treemap — D3.js v7 Starter
// Data format: hierarchical { name, children: [{ name, value }] }

import * as d3 from "d3";

const data = {
  name: "Emissions",
  children: [
    { name: "Stationary Combustion", value: 2800 },
    { name: "Electricity", value: 3200 },
    { name: "Process Emissions", value: 1500 },
    { name: "Mobile Combustion", value: 600 },
    { name: "Fugitive", value: 200 },
    { name: "Purchased Goods", value: 1100 },
    { name: "Upstream Transport", value: 450 },
    { name: "Waste", value: 320 },
  ],
};

const width = 700;
const height = 450;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet");

// Build hierarchy
const root = d3.hierarchy(data)
  .sum((d) => d.value)
  .sort((a, b) => b.value - a.value);

// Treemap layout
d3.treemap()
  .size([width, height])
  .padding(3)
  .round(true)(root);

const color = d3.scaleOrdinal(d3.schemeTableau10);

// Draw rectangles
const cell = svg.selectAll("g")
  .data(root.leaves())
  .join("g")
  .attr("transform", (d) => `translate(${d.x0},${d.y0})`);

cell.append("rect")
  .attr("width", (d) => d.x1 - d.x0)
  .attr("height", (d) => d.y1 - d.y0)
  .attr("fill", (d) => color(d.data.name))
  .attr("opacity", 0.85)
  .attr("rx", 2);

// Labels (only if cell is large enough)
cell.append("text")
  .attr("x", 6)
  .attr("y", 18)
  .style("font-size", "11px")
  .style("font-weight", "600")
  .style("fill", "#fff")
  .text((d) => {
    const w = d.x1 - d.x0;
    return w > 60 ? d.data.name : "";
  });

cell.append("text")
  .attr("x", 6)
  .attr("y", 34)
  .style("font-size", "10px")
  .style("fill", "#ffffffcc")
  .text((d) => {
    const w = d.x1 - d.x0;
    return w > 60 ? `${d.data.value} tCO2e` : "";
  });
```

## Configuration Options
- `padding` — space between cells; use `paddingInner` / `paddingOuter` for finer control
- `tile` — layout algorithm: `d3.treemapSquarify` (default), `d3.treemapBinary`, `d3.treemapSlice`
- `color` — map to parent category for grouped coloring
- `.round(true)` — pixel-aligned edges for crisp rendering

## Energy/Climate Data Example
```javascript
// Emissions by source category (tCO2e)
const data = {
  name: "Total Emissions",
  children: [
    {
      name: "Scope 1",
      children: [
        { name: "Natural Gas Combustion", value: 1800 },
        { name: "Diesel Generators", value: 600 },
        { name: "Process CO2", value: 1500 },
        { name: "Fugitive SF6", value: 200 },
      ],
    },
    {
      name: "Scope 2",
      children: [
        { name: "Grid Electricity", value: 3200 },
      ],
    },
    {
      name: "Scope 3",
      children: [
        { name: "Purchased Goods", value: 1100 },
        { name: "Transport", value: 450 },
        { name: "Waste", value: 320 },
      ],
    },
  ],
};
```

## Customization Tips
- Add drill-down by listening for clicks and re-computing layout on a child node
- Use `d3.treemapSquarify.ratio(1)` for more square-shaped cells
- Add tooltips on hover for cells too small to display labels
- Animate transitions between layouts with `d3.interpolate` on x0, y0, x1, y1

## Related
- [[Treemap]] — chart type reference
- [[Treemap — Plotly Template]] — Plotly alternative
