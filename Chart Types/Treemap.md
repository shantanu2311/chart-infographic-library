---
title: Treemap
aliases:
  - Tree Map
  - Rectangular Treemap
chart_type: treemap
category: hierarchical
data_types:
  - hierarchical
  - categorical
  - continuous
data_contexts:
  - Climate & Emissions
  - Public Finance & MDBs
  - Supply Chain & Critical Minerals
complexity: medium
audience:
  - technical
  - executive
visual_styles:
  - corporate
  - dashboard
  - editorial
color_approach: categorical
libraries:
  - d3
  - plotly
  - echarts
  - recharts
  - highcharts
  - flourish
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/composition
  - data-type/hierarchical
  - data-type/categorical
  - data-type/quantitative
  - complexity/intermediate
  - audience/analysts
  - audience/researchers
  - audience/policy-makers
  - theme/emissions
  - theme/MDBs
  - theme/critical-minerals
  - theme/supply-chain
---

# Treemap

## What It Is
A treemap displays hierarchical data as a set of nested rectangles, where each branch of the hierarchy is represented by a rectangle whose area is proportional to a quantitative variable. Color can encode a second variable or simply distinguish categories. Treemaps are especially effective when you have many categories and want to show both hierarchy and relative size simultaneously.

## Best Data Types
- Hierarchical categorical data with an associated numeric value (e.g., sector > sub-sector > emissions)
- Large datasets with many categories where bar charts would be too long
- Two-level or three-level nested compositions
- Portfolio data with grouping (theme > project > value)

## When to Use
- Visualizing how a large total is distributed across many categories and sub-categories
- Comparing relative sizes within and across groups at a glance
- Exploring hierarchical datasets interactively (drill-down treemaps)
- When space is at a premium and a long bar chart would not fit
- Showing both the forest (top-level groups) and the trees (individual items)

## When NOT to Use
> [!warning] Avoid When
> - Precise value comparison is required (rectangle areas are harder to compare than aligned bar lengths)
> - The hierarchy has more than 3 levels (readability drops sharply)
> - Categories have very similar sizes (rectangles become hard to distinguish)
> - You need to show change over time (use [[Stacked Bar Chart]] or area charts)
> - The audience is unfamiliar with treemaps and a simpler chart would suffice

## Real-World Use Cases
- Stock market visualization: sectors > industries > companies sized by market cap
- Disk space usage: folders > subfolders > files sized by bytes
- Government spending: departments > programs > line items
- News aggregation: topics > sources > article count

### Energy & Climate Applications
- Global GHG emissions by sector > sub-sector (energy, industry, agriculture, waste, LULUCF) sized by MtCO2e
- MDB climate portfolio: theme (mitigation/adaptation) > project type > individual projects sized by USD committed
- Critical mineral reserves by country > mineral type (lithium, cobalt, nickel, rare earths) sized by tonnes
- National energy consumption by end-use sector > fuel type sized by petajoules
- Carbon credit market: standard (Verra/Gold Standard) > project type > individual projects sized by credits issued

## Visual Style Variations
- **Flat treemap** — single-level rectangles colored by category, no nesting
- **Nested treemap** — two or three levels with visible borders separating parent groups
- **Interactive drill-down** — click a rectangle to zoom into its children
- **Color-encoded treemap** — rectangle color represents a second variable (e.g., growth rate, intensity)

## Related Charts
- [[Sunburst Chart]] — radial alternative for hierarchical data; better for showing path from root to leaf
- [[Marimekko Chart]] — two-dimensional bar chart that also encodes two variables in width and height
- [[Stacked Bar Chart]] — simpler alternative when hierarchy is shallow or time comparison is needed

## Inspiration Sources
- [Global Carbon Atlas](http://www.globalcarbonatlas.org/) — emissions by country and sector treemaps
- [Climate Watch Data Explorer](https://www.climatewatchdata.org/) — GHG emissions hierarchical breakdowns
- [USGS Mineral Commodity Summaries](https://www.usgs.gov/centers/national-minerals-information-center) — critical mineral reserves data
