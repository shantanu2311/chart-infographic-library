---
title: Marimekko Chart
aliases:
  - Mekko Chart
  - Mosaic Plot
  - Marimekko Plot
chart_type: marimekko-chart
category: composition
data_types:
  - categorical
  - continuous
  - proportional
data_contexts:
  - Energy Markets
  - Climate & Emissions
complexity: complex
audience:
  - technical
  - academic
visual_styles:
  - corporate
  - editorial
color_approach: categorical
libraries:
  - d3
  - plotly
  - highcharts
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/composition
  - data-type/categorical
  - data-type/quantitative
  - data-type/two-dimensional
  - complexity/advanced
  - audience/analysts
  - audience/consultants
  - audience/researchers
  - theme/emissions
  - theme/energy-transition
  - theme/MDBs
  - theme/carbon-markets
---

# Marimekko Chart

## What It Is
A Marimekko chart (also called a Mekko or Mosaic plot) is a two-dimensional stacked chart where both the width and height of segments encode data. Column widths represent one variable (e.g., market size or total emissions), while segment heights within each column represent the proportional breakdown of a second variable (e.g., fuel type or technology share). This allows two dimensions of categorical-quantitative data to be displayed simultaneously in a single compact visualization.

## Best Data Types
- Two categorical variables with an associated quantitative measure
- Market share data: segments (height) across markets of different sizes (width)
- Cross-tabulated data where both row and column totals are meaningful
- Portfolio composition where entity size varies significantly

## When to Use
- Showing market or emission shares across entities of different sizes simultaneously
- Comparing both the relative composition and absolute magnitude across groups
- Consulting-style presentations where information density is valued
- When a standard [[Stacked Bar Chart]] misses the story because bar widths are uniform but group sizes differ dramatically
- Communicating two dimensions of comparison in a single, space-efficient chart

## When NOT to Use
> [!warning] Avoid When
> - The audience is not analytically sophisticated (the dual encoding of width and height is confusing for general audiences)
> - One of the two dimensions is not meaningful or does not vary significantly
> - You have more than 6-8 columns or more than 5-6 segments per column
> - Precise value reading is required (areas are harder to judge than lengths)
> - Time-series data is involved (Marimekko charts are snapshot comparisons)

## Real-World Use Cases
- Management consulting: market share by segment across regions of different sizes
- Retail analytics: product category mix across stores of different revenue
- Healthcare: treatment distribution across patient populations of varying size
- Academic publishing: research output by field across universities of different sizes

### Energy & Climate Applications
- Global emissions by sector (column width = total sector emissions) and fuel type (segment height = fuel share within sector)
- Renewable energy market share by region (width = regional market size in GW) and technology (height = solar/wind/hydro share)
- MDB climate portfolio by geography (width = total regional lending) and theme (height = mitigation/adaptation/cross-cutting split)
- Carbon market volumes by exchange (width = total traded volume) and credit type (height = compliance/voluntary share)
- Energy investment by country (width = total investment USD) and technology category (height = fossil/renewable/nuclear/grid split)

## Visual Style Variations
- **Standard Marimekko** — variable-width columns with stacked segments, percentage labels
- **100% Marimekko** — all columns same height (100%), only width varies, emphasizing share comparison
- **Labeled Marimekko** — segment labels inside rectangles with values, consulting-presentation style
- **Color-gradient Marimekko** — segment color intensity encodes a third variable (e.g., growth rate)

## Related Charts
- [[Treemap]] — alternative for hierarchical part-of-whole data without the dual-axis encoding
- [[Stacked Bar Chart]] — simpler version where all bars have equal width; use when group size differences are not important
- [[Heatmap]] — matrix-based alternative for showing intensity across two categorical dimensions

## Inspiration Sources
- [McKinsey Global Energy Perspective](https://www.mckinsey.com/industries/oil-and-gas/our-insights/global-energy-perspective) — energy market Marimekko visualizations
- [BloombergNEF Energy Transition Investment Trends](https://about.bnef.com/) — investment by region and technology
- [ICAP Emissions Trading Worldwide Status Report](https://icapcarbonaction.com/) — carbon market volumes by jurisdiction
