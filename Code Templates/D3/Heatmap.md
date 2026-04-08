---
title: Heatmap — D3.js Template
tags:
  - code-template
  - d3
chart_type: heatmap
library: d3
---

# Heatmap — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Heatmap — D3.js v7 Starter
// Data format: [{ row: string, col: string, value: number }]

import * as d3 from "d3";

const data = [
  { row: "Jan", col: "Solar", value: 12 },
  { row: "Feb", col: "Solar", value: 18 },
  { row: "Mar", col: "Solar", value: 28 },
  { row: "Apr", col: "Solar", value: 45 },
  { row: "May", col: "Solar", value: 52 },
  { row: "Jun", col: "Solar", value: 48 },
  { row: "Jan", col: "Wind", value: 35 },
  { row: "Feb", col: "Wind", value: 30 },
  { row: "Mar", col: "Wind", value: 22 },
  { row: "Apr", col: "Wind", value: 18 },
  { row: "May", col: "Wind", value: 15 },
  { row: "Jun", col: "Wind", value: 20 },
  { row: "Jan", col: "Hydro", value: 25 },
  { row: "Feb", col: "Hydro", value: 22 },
  { row: "Mar", col: "Hydro", value: 18 },
  { row: "Apr", col: "Hydro", value: 15 },
  { row: "May", col: "Hydro", value: 30 },
  { row: "Jun", col: "Hydro", value: 42 },
];

const rows = [...new Set(data.map((d) => d.row))];
const cols = [...new Set(data.map((d) => d.col))];

const margin = { top: 30, right: 30, bottom: 50, left: 60 };
const cellSize = 60;
const width = cols.length * cellSize;
const height = rows.length * cellSize;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales
const x = d3.scaleBand().domain(cols).range([0, width]).padding(0.05);
const y = d3.scaleBand().domain(rows).range([0, height]).padding(0.05);

const colorScale = d3.scaleSequential(d3.interpolateYlOrRd)
  .domain([0, d3.max(data, (d) => d.value)]);

// Axes
svg.append("g").call(d3.axisTop(x)).select(".domain").remove();
svg.append("g").call(d3.axisLeft(y)).select(".domain").remove();

// Cells
svg.selectAll("rect")
  .data(data)
  .join("rect")
  .attr("x", (d) => x(d.col))
  .attr("y", (d) => y(d.row))
  .attr("width", x.bandwidth())
  .attr("height", y.bandwidth())
  .attr("fill", (d) => colorScale(d.value))
  .attr("rx", 3);

// Value labels inside cells
svg.selectAll(".cell-label")
  .data(data)
  .join("text")
  .attr("class", "cell-label")
  .attr("x", (d) => x(d.col) + x.bandwidth() / 2)
  .attr("y", (d) => y(d.row) + y.bandwidth() / 2)
  .attr("text-anchor", "middle")
  .attr("dy", "0.35em")
  .style("font-size", "12px")
  .style("fill", (d) => (d.value > 35 ? "#fff" : "#333"))
  .text((d) => d.value);
```

## Configuration Options
- `colorScale` — try `d3.interpolateBlues`, `d3.interpolateViridis`, `d3.interpolateRdYlGn`
- `cellSize` — fixed cell size; or use `scaleBand` with total width for responsive
- `padding` — gap between cells (0 to 1)
- Text fill contrast — flip color based on value threshold for readability

## Energy/Climate Data Example
```javascript
// Monthly capacity factor (%) by energy source
const data = [
  { row: "Jan", col: "Solar", value: 12 },
  { row: "Jan", col: "Wind", value: 35 },
  { row: "Jan", col: "Hydro", value: 25 },
  { row: "Jul", col: "Solar", value: 55 },
  { row: "Jul", col: "Wind", value: 12 },
  { row: "Jul", col: "Hydro", value: 48 },
];
```

## Customization Tips
- Add a color legend with `d3.axisBottom(d3.scaleLinear())` mapped to the gradient
- Use `d3.interpolateRdYlGn` (diverging) for data centered around zero
- Add tooltip on hover showing row, column, and exact value
- For large matrices, remove cell labels and rely on color + tooltip

## Related
- [[Heatmap]] — chart type reference
- [[Heatmap — Plotly Template]] — Plotly alternative
