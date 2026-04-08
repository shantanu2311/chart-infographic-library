---
title: Sankey Diagram — D3.js Template
tags:
  - code-template
  - d3
chart_type: sankey-diagram
library: d3
---

# Sankey Diagram — D3.js

## Setup
```bash
npm install d3 d3-sankey
```

## Basic Template
```javascript
// Sankey Diagram — D3.js v7 + d3-sankey Starter
// Data format: { nodes: [{ name }], links: [{ source, target, value }] }

import * as d3 from "d3";
import { sankey, sankeyLinkHorizontal } from "d3-sankey";

const data = {
  nodes: [
    { name: "Coal" },
    { name: "Natural Gas" },
    { name: "Solar" },
    { name: "Wind" },
    { name: "Power Plant" },
    { name: "Grid" },
    { name: "Industry" },
    { name: "Residential" },
    { name: "Transport" },
  ],
  links: [
    { source: 0, target: 4, value: 500 },
    { source: 1, target: 4, value: 200 },
    { source: 2, target: 5, value: 120 },
    { source: 3, target: 5, value: 80 },
    { source: 4, target: 5, value: 650 },
    { source: 5, target: 6, value: 400 },
    { source: 5, target: 7, value: 300 },
    { source: 5, target: 8, value: 150 },
  ],
};

const width = 800;
const height = 450;
const margin = { top: 10, right: 10, bottom: 10, left: 10 };

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet");

// Sankey layout
const sankeyLayout = sankey()
  .nodeWidth(20)
  .nodePadding(15)
  .extent([[margin.left, margin.top], [width - margin.right, height - margin.bottom]]);

const { nodes, links } = sankeyLayout(data);

const color = d3.scaleOrdinal(d3.schemeTableau10);

// Draw links
svg.append("g")
  .selectAll("path")
  .data(links)
  .join("path")
  .attr("d", sankeyLinkHorizontal())
  .attr("fill", "none")
  .attr("stroke", (d) => color(d.source.name))
  .attr("stroke-opacity", 0.4)
  .attr("stroke-width", (d) => Math.max(1, d.width));

// Draw nodes
svg.append("g")
  .selectAll("rect")
  .data(nodes)
  .join("rect")
  .attr("x", (d) => d.x0)
  .attr("y", (d) => d.y0)
  .attr("width", (d) => d.x1 - d.x0)
  .attr("height", (d) => d.y1 - d.y0)
  .attr("fill", (d) => color(d.name))
  .attr("rx", 2);

// Node labels
svg.append("g")
  .selectAll("text")
  .data(nodes)
  .join("text")
  .attr("x", (d) => (d.x0 < width / 2 ? d.x1 + 8 : d.x0 - 8))
  .attr("y", (d) => (d.y0 + d.y1) / 2)
  .attr("dy", "0.35em")
  .attr("text-anchor", (d) => (d.x0 < width / 2 ? "start" : "end"))
  .style("font-size", "12px")
  .text((d) => d.name);
```

## Configuration Options
- `nodeWidth` — width of node rectangles in pixels
- `nodePadding` — vertical space between nodes
- `sankeyLayout.iterations(32)` — more iterations = better node positioning
- Link color — try coloring by source, target, or a gradient between both

## Energy/Climate Data Example
```javascript
// Energy flow: sources -> conversion -> end use (TWh)
const data = {
  nodes: [
    { name: "Coal" }, { name: "Gas" }, { name: "Solar" },
    { name: "Thermal Plant" }, { name: "Grid" },
    { name: "Steel Mill" }, { name: "Cement Plant" }, { name: "Residential" },
  ],
  links: [
    { source: 0, target: 3, value: 1000 },
    { source: 1, target: 3, value: 200 },
    { source: 2, target: 4, value: 120 },
    { source: 3, target: 4, value: 1100 },
    { source: 4, target: 5, value: 500 },
    { source: 4, target: 6, value: 300 },
    { source: 4, target: 7, value: 420 },
  ],
};
```

## Customization Tips
- Add link gradients with `linearGradient` for source-to-target color blending
- Implement node dragging with `d3.drag()` for repositioning
- Highlight connected paths on hover by filtering links by source/target
- For circular flows, use `d3-sankey-circular` instead

## Related
- [[Sankey Diagram]] — chart type reference
- [[Sankey Diagram — Plotly Template]] — Plotly alternative
