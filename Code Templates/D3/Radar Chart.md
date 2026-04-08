---
title: Radar Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: radar-chart
library: d3
---

# Radar Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Radar Chart — D3.js v7 Starter
// Data format: [{ axis: string, value: number }] per series

import * as d3 from "d3";

const axes = [
  "Energy Efficiency",
  "Renewable Share",
  "Waste Reduction",
  "Water Recycling",
  "Process Optimization",
  "Emission Intensity",
];

const series = [
  { name: "Plant A", values: [0.72, 0.45, 0.68, 0.55, 0.80, 0.60] },
  { name: "Plant B", values: [0.55, 0.78, 0.42, 0.70, 0.50, 0.85] },
];

const width = 500;
const height = 500;
const radius = Math.min(width, height) / 2 - 60;
const levels = 5; // number of concentric rings
const angleSlice = (Math.PI * 2) / axes.length;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${width / 2},${height / 2})`);

const rScale = d3.scaleLinear().domain([0, 1]).range([0, radius]);
const color = d3.scaleOrdinal().domain(series.map((s) => s.name)).range(["#2563eb", "#e63946"]);

// Concentric grid circles
for (let i = 1; i <= levels; i++) {
  svg.append("circle")
    .attr("r", (radius / levels) * i)
    .attr("fill", "none")
    .attr("stroke", "#ddd")
    .attr("stroke-dasharray", "2,2");
}

// Axis lines and labels
axes.forEach((axis, i) => {
  const angle = angleSlice * i - Math.PI / 2;
  const x = Math.cos(angle) * radius;
  const y = Math.sin(angle) * radius;

  svg.append("line")
    .attr("x1", 0).attr("y1", 0)
    .attr("x2", x).attr("y2", y)
    .attr("stroke", "#ccc");

  svg.append("text")
    .attr("x", Math.cos(angle) * (radius + 20))
    .attr("y", Math.sin(angle) * (radius + 20))
    .attr("text-anchor", "middle")
    .attr("dy", "0.35em")
    .style("font-size", "11px")
    .text(axis);
});

// Radar line generator
const radarLine = d3.lineRadial()
  .radius((d) => rScale(d))
  .angle((d, i) => i * angleSlice)
  .curve(d3.curveLinearClosed);

// Draw each series
series.forEach((s) => {
  // Filled area
  svg.append("path")
    .datum(s.values)
    .attr("d", radarLine)
    .attr("fill", color(s.name))
    .attr("fill-opacity", 0.15)
    .attr("stroke", color(s.name))
    .attr("stroke-width", 2);

  // Data points
  s.values.forEach((val, i) => {
    const angle = angleSlice * i - Math.PI / 2;
    svg.append("circle")
      .attr("cx", Math.cos(angle) * rScale(val))
      .attr("cy", Math.sin(angle) * rScale(val))
      .attr("r", 4)
      .attr("fill", color(s.name));
  });
});

// Legend
series.forEach((s, i) => {
  const g = svg.append("g").attr("transform", `translate(${-width / 2 + 20},${-height / 2 + 20 + i * 22})`);
  g.append("rect").attr("width", 14).attr("height", 14).attr("fill", color(s.name)).attr("rx", 2);
  g.append("text").attr("x", 20).attr("y", 12).style("font-size", "12px").text(s.name);
});
```

## Configuration Options
- `levels` — number of concentric grid rings
- `rScale.domain()` — adjust max value (default [0, 1] for normalized data)
- `curve` — `d3.curveLinearClosed` for sharp, `d3.curveCardinalClosed` for smooth
- `fill-opacity` — transparency of the filled area per series

## Energy/Climate Data Example
```javascript
// Sustainability performance scores (0-1 normalized)
const axes = [
  "Energy Efficiency",
  "Renewable Share",
  "Waste Reduction",
  "Water Recycling",
  "Process Optimization",
  "Emission Intensity",
];

const series = [
  { name: "Current", values: [0.55, 0.30, 0.50, 0.45, 0.60, 0.40] },
  { name: "Target 2030", values: [0.85, 0.75, 0.80, 0.70, 0.90, 0.80] },
];
```

## Customization Tips
- Normalize all values to 0-1 range before plotting for fair comparison
- Add interactive hover: highlight one series and dim others
- Use `d3.curveCardinalClosed.tension(0.5)` for smoother radar shapes
- Add value labels next to data points for exact readings

## Related
- [[Radar Chart]] — chart type reference
- [[Radar Chart — Plotly Template]] — Plotly alternative
