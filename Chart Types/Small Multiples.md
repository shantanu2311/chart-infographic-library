---
title: Small Multiples
aliases:
  - Trellis Chart
  - Panel Chart
  - Lattice Plot
tags:
  - chart-type/pattern
  - data-type/time-series
  - data-type/categorical
  - data-type/comparative
  - complexity/intermediate
  - audience/analyst
  - audience/researcher
  - audience/executive
  - theme/energy
  - theme/climate
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/esg
category: Pattern
complexity: intermediate
best_audience: analysts, researchers, executives
---

# Small Multiples

## What It Is
Small multiples are a grid of identical mini-charts, each displaying a different subset of the data (a different facility, country, technology, or category) using the same axes, scales, and visual encoding. Coined by Edward Tufte, the technique leverages the eye's ability to detect pattern differences across a consistent visual framework. Instead of overlaying 10 lines on one cluttered chart, you place 10 clean charts side by side, making comparison effortless.

## Best Data Types
- One base chart type (line, bar, area) replicated across a categorical dimension
- Time series for multiple entities sharing the same date range
- Any dataset where a faceting variable splits data into 4-25 comparable subsets
- Panel data: same metrics measured for different groups over time

## When to Use
- Comparing trends across many entities without spaghetti-line overlap
- When a single chart with 10+ series becomes unreadable
- Showing that a pattern (or anomaly) is consistent or unique across subsets
- Enabling the reader to scan for outliers in a grid of otherwise similar shapes
- When consistent axes matter more than space efficiency

## When NOT to Use
> [!warning] Avoid When
> - You have fewer than 3 subsets (just overlay them on one chart)
> - The subsets need to be compared at exact intersecting points (overlay is better)
> - You have more than 25 panels (the grid becomes too small to read)
> - Each subset has fundamentally different scales (shared axes become meaningless)
> - Space is extremely limited (small multiples require generous layout)

## Real-World Use Cases
- Sparkline grids in financial dashboards showing each stock's 52-week trend
- Weather pattern comparison across cities (temperature, precipitation)
- A/B test results shown per user segment
- Edward Tufte's original examples in "The Visual Display of Quantitative Information"

### Energy & Climate Applications
- Emission trends for each of 10 industrial facilities on shared axes
- Carbon price across 8 ETS markets (EU, UK, China, Korea, California, RGGI, NZ, Mexico)
- Renewable generation by technology across 6 countries (solar, wind, hydro panels)
- Temperature anomaly by region showing climate change signal consistency
- Grid frequency stability across 5 regional grids in India (NR, WR, SR, ER, NER)

## Visual Style Variations
- **Line grid** — mini line charts in rows and columns, most common form
- **Bar grid** — mini bar charts per category, good for ranking within each panel
- **Area grid** — filled area charts showing volume patterns across panels
- **Map grid** — mini choropleth maps for each time period (geographic small multiples)

## Related Charts
- [[Line Chart]] — the single-panel version; small multiples decompose a crowded line chart
- [[Bar Chart]] — when each panel shows a bar comparison instead of a trend
- [[Area Chart]] — filled version for volume emphasis in each panel
- [[Sparkline]] — extreme miniaturization of the same principle, embedded inline

## Tools That Support This
- **Datawrapper** — small multiples as a built-in chart type
- **ggplot2** — `facet_wrap()` and `facet_grid()` for effortless panel creation
- **D3.js** — manual panel layout with shared scales
- **Tableau** — small multiples via row/column shelf faceting

## Inspiration Sources
- [Datawrapper Small Multiples Guide](https://blog.datawrapper.de/small-multiples/) — design principles and examples
- [Edward Tufte, "The Visual Display of Quantitative Information"](https://www.edwardtufte.com/tufte/books_vdqi) — the foundational text on small multiples
