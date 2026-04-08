---
title: Stacked Bar Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: stacked-bar-chart
library: d3
---

# Stacked Bar Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Stacked Bar Chart — D3.js v7 Starter
// Data format: [{ group: string, series1: number, series2: number, ... }]

import * as d3 from "d3";

const data = [
  { facility: "Plant A", scope1: 3200, scope2: 2100, scope3: 1800 },
  { facility: "Plant B", scope1: 2500, scope2: 3400, scope3: 1200 },
  { facility: "Plant C", scope1: 1800, scope2: 1600, scope3: 2200 },
  { facility: "Plant D", scope1: 4100, scope2: 2800, scope3: 900 },
];

const keys = ["scope1", "scope2", "scope3"];
const labels = { scope1: "Scope 1", scope2: "Scope 2", scope3: "Scope 3" };
const colors = ["#e63946", "#457b9d", "#2a9d8f"];

const stack = d3.stack().keys(keys);
const series = stack(data);

const margin = { top: 20, right: 120, bottom: 40, left: 60 };
const width = 600 - margin.left - margin.right;
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
  .domain(data.map((d) => d.facility))
  .range([0, width])
  .padding(0.25);

const y = d3.scaleLinear()
  .domain([0, d3.max(series, (s) => d3.max(s, (d) => d[1]))])
  .nice()
  .range([height, 0]);

const color = d3.scaleOrdinal().domain(keys).range(colors);

// Axes
svg.append("g").attr("transform", `translate(0,${height})`).call(d3.axisBottom(x));
svg.append("g").call(d3.axisLeft(y));

// Stacked bars
svg.selectAll("g.series")
  .data(series)
  .join("g")
  .attr("class", "series")
  .attr("fill", (d) => color(d.key))
  .selectAll("rect")
  .data((d) => d)
  .join("rect")
  .attr("x", (d) => x(d.data.facility))
  .attr("y", (d) => y(d[1]))
  .attr("height", (d) => y(d[0]) - y(d[1]))
  .attr("width", x.bandwidth())
  .attr("rx", 1);

// Legend
keys.forEach((key, i) => {
  const g = svg.append("g").attr("transform", `translate(${width + 15}, ${i * 24})`);
  g.append("rect").attr("width", 16).attr("height", 16).attr("fill", colors[i]).attr("rx", 3);
  g.append("text").attr("x", 22).attr("y", 13).text(labels[key]).style("font-size", "12px");
});
```

## Configuration Options
- `stack.order()` — `d3.stackOrderAscending` to put smallest on bottom
- `stack.offset()` — `d3.stackOffsetExpand` for 100% stacked (normalized)
- `padding` — space between groups of bars
- Change to horizontal by swapping x/y scales (Band on y, Linear on x)

## Energy/Climate Data Example
```javascript
// Emissions by facility and scope (tCO2e)
const data = [
  { facility: "EAF Unit", scope1: 3200, scope2: 2100, scope3: 1800 },
  { facility: "Induction", scope1: 2500, scope2: 3400, scope3: 1200 },
  { facility: "Re-rolling", scope1: 1800, scope2: 1600, scope3: 2200 },
  { facility: "Forge Shop", scope1: 4100, scope2: 2800, scope3: 900 },
];
```

## Customization Tips
- Add value labels inside segments when height > threshold
- Toggle to grouped bar (side-by-side) by using `d3.scaleBand` within each group
- Add total labels above each stacked column
- Animate with `.transition().duration(600).attr("y", ...)` on enter

## Related
- [[Stacked Bar Chart]] — chart type reference
- [[Stacked Bar Chart — Plotly Template]] — Plotly alternative
