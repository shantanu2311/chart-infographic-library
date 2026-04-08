---
title: Line Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: line-chart
library: d3
---

# Line Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Line Chart — D3.js v7 Starter
// Data format: [{ date: string (YYYY-MM-DD), value: number }]

import * as d3 from "d3";

const data = [
  { date: "2020-01-01", value: 750 },
  { date: "2021-01-01", value: 710 },
  { date: "2022-01-01", value: 680 },
  { date: "2023-01-01", value: 640 },
  { date: "2024-01-01", value: 590 },
  { date: "2025-01-01", value: 530 },
];

// Parse dates
const parseDate = d3.timeParse("%Y-%m-%d");
data.forEach((d) => (d.date = parseDate(d.date)));

// Dimensions
const margin = { top: 20, right: 30, bottom: 40, left: 60 };
const width = 700 - margin.left - margin.right;
const height = 400 - margin.top - margin.bottom;

// Responsive SVG
const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales
const x = d3.scaleTime()
  .domain(d3.extent(data, (d) => d.date))
  .range([0, width]);

const y = d3.scaleLinear()
  .domain([0, d3.max(data, (d) => d.value)])
  .nice()
  .range([height, 0]);

// Axes
svg.append("g")
  .attr("transform", `translate(0,${height})`)
  .call(d3.axisBottom(x).ticks(6));

svg.append("g").call(d3.axisLeft(y));

// Line generator
const line = d3.line()
  .x((d) => x(d.date))
  .y((d) => y(d.value))
  .curve(d3.curveMonotoneX); // smooth interpolation

// Draw line
svg.append("path")
  .datum(data)
  .attr("fill", "none")
  .attr("stroke", "#2563eb")
  .attr("stroke-width", 2.5)
  .attr("d", line);

// Data points
svg.selectAll("circle")
  .data(data)
  .join("circle")
  .attr("cx", (d) => x(d.date))
  .attr("cy", (d) => y(d.value))
  .attr("r", 4)
  .attr("fill", "#2563eb");
```

## Configuration Options
- `curve` — interpolation style: `d3.curveLinear`, `d3.curveMonotoneX`, `d3.curveBasis`
- `stroke-width` — line thickness
- `ticks` — number of axis ticks; use `.tickFormat(d3.timeFormat("%Y"))` for custom labels
- `.nice()` — rounds domain to clean values

## Energy/Climate Data Example
```javascript
// India grid emission factor trend (tCO2/MWh)
const data = [
  { date: "2017-01-01", value: 0.92 },
  { date: "2018-01-01", value: 0.90 },
  { date: "2019-01-01", value: 0.88 },
  { date: "2020-01-01", value: 0.85 },
  { date: "2021-01-01", value: 0.82 },
  { date: "2022-01-01", value: 0.79 },
  { date: "2023-01-01", value: 0.76 },
  { date: "2024-01-01", value: 0.71 },
];
```

## Customization Tips
- Add area fill below the line with `d3.area()` and a low-opacity fill
- Multi-line: loop over series and use `d3.scaleOrdinal(d3.schemeCategory10)` for colors
- Add crosshair tooltip with `bisector` for nearest-point lookup on mousemove
- Animate line drawing with `stroke-dasharray` and `stroke-dashoffset` transition

## Related
- [[Line Chart]] — chart type reference
- [[Line Chart — Plotly Template]] — Plotly alternative
