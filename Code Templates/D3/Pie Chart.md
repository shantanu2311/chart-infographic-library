---
title: Pie Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: pie-chart
library: d3
---

# Pie Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Pie Chart — D3.js v7 Starter
// Data format: [{ label: string, value: number }]

import * as d3 from "d3";

const data = [
  { label: "Scope 1", value: 4500 },
  { label: "Scope 2", value: 3200 },
  { label: "Scope 3", value: 2100 },
];

const width = 500;
const height = 400;
const radius = Math.min(width, height) / 2 - 20;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${width / 2},${height / 2})`);

const color = d3.scaleOrdinal()
  .domain(data.map((d) => d.label))
  .range(["#e63946", "#457b9d", "#2a9d8f"]);

// Pie layout + arc generator
const pie = d3.pie()
  .value((d) => d.value)
  .sort(null); // keep original order

const arc = d3.arc()
  .innerRadius(0)
  .outerRadius(radius);

const labelArc = d3.arc()
  .innerRadius(radius * 0.6)
  .outerRadius(radius * 0.6);

// Draw slices
svg.selectAll("path")
  .data(pie(data))
  .join("path")
  .attr("d", arc)
  .attr("fill", (d) => color(d.data.label))
  .attr("stroke", "#fff")
  .attr("stroke-width", 2);

// Labels
svg.selectAll("text")
  .data(pie(data))
  .join("text")
  .attr("transform", (d) => `translate(${labelArc.centroid(d)})`)
  .attr("text-anchor", "middle")
  .style("font-size", "13px")
  .style("font-weight", "600")
  .style("fill", "#fff")
  .text((d) => `${d.data.label} (${d.data.value})`);
```

## Configuration Options
- `innerRadius` — set > 0 for donut chart (e.g., `radius * 0.5`)
- `padAngle` — add `pie.padAngle(0.02)` for gaps between slices
- `sort` — `null` preserves order; omit for descending sort by value
- `cornerRadius` — add `arc.cornerRadius(4)` for rounded slice edges

## Energy/Climate Data Example
```javascript
// Emission breakdown by scope (tCO2e)
const data = [
  { label: "Scope 1 — Direct", value: 4500 },
  { label: "Scope 2 — Electricity", value: 3200 },
  { label: "Scope 3 — Value Chain", value: 2100 },
];
```

## Customization Tips
- Add hover effect: scale up arc on mouseover with `arc.outerRadius(radius + 10)`
- Use polyline leaders for labels on small slices instead of centroid text
- Animate slices with `attrTween("d", arcTween)` for smooth transitions
- Add a center text element for donut charts to show the total

## Related
- [[Pie Chart]] — chart type reference
- [[Pie Chart — Plotly Template]] — Plotly alternative
