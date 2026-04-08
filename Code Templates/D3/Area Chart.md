---
title: Area Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: area-chart
library: d3
---

# Area Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Stacked Area Chart — D3.js v7 Starter
// Data format: [{ date: string, series1: number, series2: number, ... }]

import * as d3 from "d3";

const data = [
  { date: "2019", coal: 1028, gas: 62, solar: 39, wind: 65 },
  { date: "2020", coal: 966, gas: 60, solar: 54, wind: 68 },
  { date: "2021", coal: 1052, gas: 63, solar: 73, wind: 72 },
  { date: "2022", coal: 1098, gas: 66, solar: 91, wind: 76 },
  { date: "2023", coal: 1078, gas: 68, solar: 113, wind: 82 },
];

const keys = ["coal", "gas", "solar", "wind"];
const colors = ["#4a4a4a", "#7eb0d5", "#f7c948", "#5ab47a"];

// Stack generator
const stack = d3.stack().keys(keys).order(d3.stackOrderNone).offset(d3.stackOffsetNone);
const series = stack(data);

// Dimensions
const margin = { top: 20, right: 120, bottom: 40, left: 60 };
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
const x = d3.scalePoint()
  .domain(data.map((d) => d.date))
  .range([0, width]);

const y = d3.scaleLinear()
  .domain([0, d3.max(series, (s) => d3.max(s, (d) => d[1]))])
  .nice()
  .range([height, 0]);

const color = d3.scaleOrdinal().domain(keys).range(colors);

// Axes
svg.append("g").attr("transform", `translate(0,${height})`).call(d3.axisBottom(x));
svg.append("g").call(d3.axisLeft(y));

// Area generator
const area = d3.area()
  .x((d) => x(d.data.date))
  .y0((d) => y(d[0]))
  .y1((d) => y(d[1]))
  .curve(d3.curveMonotoneX);

// Draw stacked areas
svg.selectAll(".area")
  .data(series)
  .join("path")
  .attr("class", "area")
  .attr("d", area)
  .attr("fill", (d) => color(d.key))
  .attr("opacity", 0.85);

// Legend
keys.forEach((key, i) => {
  const g = svg.append("g").attr("transform", `translate(${width + 15}, ${i * 22})`);
  g.append("rect").attr("width", 14).attr("height", 14).attr("fill", colors[i]);
  g.append("text").attr("x", 20).attr("y", 12).text(key).style("font-size", "12px");
});
```

## Configuration Options
- `stack.offset()` — try `d3.stackOffsetExpand` for 100% stacked, `d3.stackOffsetWiggle` for streamgraph
- `stack.order()` — `d3.stackOrderInsideOut` for streamgraph aesthetics
- `curve` — smoothing: `d3.curveMonotoneX`, `d3.curveBasis`, `d3.curveStep`
- `opacity` — layer transparency for overlapping readability

## Energy/Climate Data Example
```javascript
// India electricity generation mix (TWh) by year
const data = [
  { date: "2019", coal: 1028, gas: 62, solar: 39, wind: 65, hydro: 162 },
  { date: "2020", coal: 966, gas: 60, solar: 54, wind: 68, hydro: 155 },
  { date: "2021", coal: 1052, gas: 63, solar: 73, wind: 72, hydro: 151 },
  { date: "2022", coal: 1098, gas: 66, solar: 91, wind: 76, hydro: 158 },
  { date: "2023", coal: 1078, gas: 68, solar: 113, wind: 82, hydro: 162 },
];
```

## Customization Tips
- Add line borders on top of areas: draw `d3.line()` paths after areas
- Hover interaction: reduce opacity of non-hovered layers on mouseover
- Use `d3.stackOffsetExpand` to show proportional (percentage) view
- Animate with `.transition().duration(800)` on the path `d` attribute

## Related
- [[Area Chart]] — chart type reference
- [[Area Chart — Plotly Template]] — Plotly alternative
