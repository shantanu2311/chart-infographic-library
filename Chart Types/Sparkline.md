---
title: Sparkline
aliases:
  - Inline Chart
  - Word-Sized Graphic
chart_type: sparkline
category: temporal
data_types:
  - time-series
data_contexts:
  - Energy Markets
  - Carbon Markets
  - Financial Markets
complexity: simple
audience:
  - executive
  - technical
visual_styles:
  - minimal
  - corporate
  - dashboard
color_approach: monochrome
libraries:
  - d3
  - recharts
  - highcharts
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/micro
  - data-type/time-series
  - data-type/trend
  - complexity/beginner
  - audience/analyst
  - audience/executive
  - audience/operations
  - theme/energy
  - theme/climate
  - theme/carbon-markets
  - theme/finance
---

# Sparkline

## What It Is
A sparkline is a tiny, word-sized chart — typically a line, bar, or area — embedded directly within text, tables, or dashboards without axes, labels, or gridlines. Coined by Edward Tufte as "data-intense, design-simple, word-sized graphics," sparklines communicate the general shape of a trend (rising, falling, volatile, stable) in the minimum possible space. They sacrifice precision for density, enabling dozens of trends to be scanned in a single table view.

## Best Data Types
- Time series reduced to shape and direction (up, down, volatile)
- Any metric where the trend matters more than individual values
- Table cell data where each row needs an inline trend indicator
- High-density dashboards with many KPIs needing trend context

## When to Use
- Embedding trend context inside a data table (one sparkline per row)
- Dashboard KPI cards showing the trend alongside the current number
- Reports where space is limited but trend context adds value
- Comparing the shape of many trends at a glance (all sparklines in a column)
- When the reader only needs to know direction and volatility, not exact values

## When NOT to Use
> [!warning] Avoid When
> - The reader needs to read specific values from the chart
> - The trend has important events that need annotation
> - The sparkline will be the only representation of the data (too little detail)
> - The time series is too short (fewer than 5 points) to show meaningful shape
> - Color or size encoding is needed beyond simple line shape

## Real-World Use Cases
- Stock tickers with 52-week sparklines next to current price
- Fitness tracker dashboards with weekly activity sparklines
- Email subject line or notification previews with inline metric trends
- Edward Tufte's original medical monitoring examples (glucose, heart rate)

### Energy & Climate Applications
- Emission trend sparklines in a country comparison table (one per row, same scale)
- Carbon price mini-trends in a portfolio dashboard alongside position value
- Inline generation trends in grid operator daily reports (one sparkline per plant)
- Temperature anomaly sparklines per decade in a climate change summary table
- Facility energy intensity sparklines alongside current performance metrics

## Visual Style Variations
- **Line sparkline** — simple polyline showing trend direction and shape
- **Bar sparkline** — tiny bars for discrete period comparisons (monthly volumes)
- **Win/loss sparkline** — binary up/down bars showing positive/negative periods
- **Area sparkline** — filled line for visual weight in high-density tables

## Related Charts
- [[Line Chart]] — full-sized version with axes, labels, and annotations
- [[Bar Chart]] — full-sized bar equivalent of bar sparklines
- [[Area Chart]] — full-sized filled trend chart
- [[Small Multiples]] — when sparklines need more room, they become small multiples

## Tools That Support This
- **Excel** — built-in sparkline feature in cells (line, column, win/loss)
- **Tableau** — sparklines via sheet-in-tooltip or small chart formatting
- **D3.js** — SVG sparkline generation with minimal markup
- **Tufte CSS** — CSS framework inspired by Tufte's design principles, including sparklines

## Inspiration Sources
- [Edward Tufte, "Beautiful Evidence"](https://www.edwardtufte.com/tufte/books_be) — the definitive text on sparklines
- [Tufte CSS Sparklines](https://edwardtufte.github.io/tufte-css/) — web implementation of Tufte's sparkline principles
