---
title: Donut Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: donut-chart
library: d3
---

# Donut Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Donut Chart — D3.js v7 Starter
// Data format: [{ label: string, value: number }]

import * as d3 from "d3";

const data = [
  { label: "Coal", value: 1042 },
  { label: "Gas", value: 68 },
  { label: "Solar", value: 113 },
  { label: "Wind", value: 82 },
  { label: "Hydro", value: 162 },
  { label: "Nuclear", value: 47 },
];

const width = 500;
const height = 420;
const outerRadius = Math.min(width, height) / 2 - 30;
const innerRadius = outerRadius * 0.55; // donut hole ratio

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${width / 2},${height / 2})`);

const color = d3.scaleOrdinal()
  .domain(data.map((d) => d.label))
  .range(["#4a4a4a", "#7eb0d5", "#f7c948", "#5ab47a", "#3a86a8", "#9b59b6"]);

const pie = d3.pie()
  .value((d) => d.value)
  .sort(null)
  .padAngle(0.02);

const arc = d3.arc().innerRadius(innerRadius).outerRadius(outerRadius).cornerRadius(4);
const labelArc = d3.arc().innerRadius(outerRadius * 0.8).outerRadius(outerRadius * 0.8);

// Slices
svg.selectAll("path")
  .data(pie(data))
  .join("path")
  .attr("d", arc)
  .attr("fill", (d) => color(d.data.label))
  .attr("stroke", "#fff")
  .attr("stroke-width", 1);

// Percentage labels on slices
const total = d3.sum(data, (d) => d.value);
svg.selectAll(".slice-label")
  .data(pie(data))
  .join("text")
  .attr("class", "slice-label")
  .attr("transform", (d) => `translate(${labelArc.centroid(d)})`)
  .attr("text-anchor", "middle")
  .style("font-size", "11px")
  .style("fill", "#fff")
  .style("font-weight", "600")
  .text((d) => {
    const pct = ((d.data.value / total) * 100).toFixed(0);
    return pct > 4 ? `${pct}%` : "";
  });

// Center text — total value
svg.append("text")
  .attr("text-anchor", "middle")
  .attr("dy", "-0.2em")
  .style("font-size", "28px")
  .style("font-weight", "700")
  .text(total.toLocaleString());

svg.append("text")
  .attr("text-anchor", "middle")
  .attr("dy", "1.2em")
  .style("font-size", "13px")
  .style("fill", "#666")
  .text("TWh Total");
```

## Configuration Options
- `innerRadius` — ratio of `outerRadius * 0.55` creates a classic donut; adjust for thinner/thicker ring
- `padAngle` — gap between slices (in radians)
- `cornerRadius` — rounded corners on arc segments
- Center text — use for total, label, or KPI display

## Energy/Climate Data Example
```javascript
// India electricity generation mix (TWh)
const data = [
  { label: "Coal", value: 1042 },
  { label: "Gas", value: 68 },
  { label: "Solar", value: 113 },
  { label: "Wind", value: 82 },
  { label: "Hydro", value: 162 },
  { label: "Nuclear", value: 47 },
];
```

## Customization Tips
- Add outer labels with polyline leaders for small slices
- Animate entry with `attrTween("d", ...)` interpolating from `{startAngle: 0, endAngle: 0}`
- Add hover effect: enlarge slice with `arc.outerRadius(outerRadius + 8)` on mouseover
- Nested donuts: add a second `arc` generator with different inner/outer radius

## Related
- [[Donut Chart]] — chart type reference
- [[Donut Chart — Plotly Template]] — Plotly alternative
