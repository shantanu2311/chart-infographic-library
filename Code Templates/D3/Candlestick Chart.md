---
title: Candlestick Chart — D3.js Template
tags:
  - code-template
  - d3
chart_type: candlestick-chart
library: d3
---

# Candlestick Chart — D3.js

## Setup
```bash
npm install d3
```

## Basic Template
```javascript
// Candlestick Chart — D3.js v7 Starter
// Data format: [{ date: string, open: number, high: number, low: number, close: number }]

import * as d3 from "d3";

const data = [
  { date: "2024-01-02", open: 82.5, high: 86.0, low: 80.1, close: 84.3 },
  { date: "2024-01-03", open: 84.3, high: 88.2, low: 83.5, close: 87.1 },
  { date: "2024-01-04", open: 87.1, high: 89.0, low: 84.0, close: 85.2 },
  { date: "2024-01-05", open: 85.2, high: 87.5, low: 82.0, close: 83.0 },
  { date: "2024-01-08", open: 83.0, high: 85.8, low: 81.5, close: 85.5 },
  { date: "2024-01-09", open: 85.5, high: 90.2, low: 85.0, close: 89.8 },
  { date: "2024-01-10", open: 89.8, high: 92.5, low: 88.0, close: 91.0 },
  { date: "2024-01-11", open: 91.0, high: 93.0, low: 87.5, close: 88.2 },
  { date: "2024-01-12", open: 88.2, high: 90.0, low: 86.0, close: 89.5 },
  { date: "2024-01-15", open: 89.5, high: 94.0, low: 89.0, close: 93.2 },
];

const parseDate = d3.timeParse("%Y-%m-%d");
data.forEach((d) => (d.date = parseDate(d.date)));

const margin = { top: 20, right: 30, bottom: 40, left: 60 };
const width = 700 - margin.left - margin.right;
const height = 400 - margin.top - margin.bottom;
const candleWidth = width / data.length * 0.6;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width + margin.left + margin.right} ${height + margin.top + margin.bottom}`)
  .attr("preserveAspectRatio", "xMidYMid meet")
  .append("g")
  .attr("transform", `translate(${margin.left},${margin.top})`);

// Scales
const x = d3.scaleBand()
  .domain(data.map((d) => d.date))
  .range([0, width])
  .padding(0.3);

const y = d3.scaleLinear()
  .domain([
    d3.min(data, (d) => d.low) * 0.98,
    d3.max(data, (d) => d.high) * 1.02,
  ])
  .range([height, 0]);

// Axes
svg.append("g")
  .attr("transform", `translate(0,${height})`)
  .call(d3.axisBottom(x).tickFormat(d3.timeFormat("%b %d")));

svg.append("g").call(d3.axisLeft(y));

// Wicks (high-low line)
svg.selectAll(".wick")
  .data(data)
  .join("line")
  .attr("class", "wick")
  .attr("x1", (d) => x(d.date) + x.bandwidth() / 2)
  .attr("x2", (d) => x(d.date) + x.bandwidth() / 2)
  .attr("y1", (d) => y(d.high))
  .attr("y2", (d) => y(d.low))
  .attr("stroke", (d) => (d.close >= d.open ? "#22c55e" : "#ef4444"))
  .attr("stroke-width", 1.5);

// Bodies (open-close rect)
svg.selectAll(".candle")
  .data(data)
  .join("rect")
  .attr("class", "candle")
  .attr("x", (d) => x(d.date))
  .attr("y", (d) => y(Math.max(d.open, d.close)))
  .attr("width", x.bandwidth())
  .attr("height", (d) => Math.max(1, Math.abs(y(d.open) - y(d.close))))
  .attr("fill", (d) => (d.close >= d.open ? "#22c55e" : "#ef4444"))
  .attr("rx", 1);
```

## Configuration Options
- Candle colors — green/red for up/down; use `#22c55e` / `#ef4444` or custom
- `x.padding()` — spacing between candles
- `y.domain()` — add 2% padding above/below high/low range
- Wick stroke-width — thinner than candle body for visual clarity

## Energy/Climate Data Example
```javascript
// EU Carbon Credit price (EUR/tCO2) — weekly OHLC
const data = [
  { date: "2024-01-08", open: 72.5, high: 76.0, low: 70.1, close: 74.3 },
  { date: "2024-01-15", open: 74.3, high: 78.2, low: 73.5, close: 77.1 },
  { date: "2024-01-22", open: 77.1, high: 79.0, low: 74.0, close: 75.2 },
  { date: "2024-01-29", open: 75.2, high: 77.5, low: 72.0, close: 73.0 },
  { date: "2024-02-05", open: 73.0, high: 75.8, low: 71.5, close: 75.5 },
];
```

## Customization Tips
- Add volume bars below as a secondary y-axis with smaller height
- Overlay a moving average line with `d3.line()` for trend indication
- Add crosshair on mousemove with vertical + horizontal guide lines
- For intraday data, use `d3.scaleTime()` instead of `scaleBand`

## Related
- [[Candlestick Chart]] — chart type reference
- [[Candlestick Chart — Plotly Template]] — Plotly alternative
