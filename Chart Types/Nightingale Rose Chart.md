---
title: Nightingale Rose Chart
aliases:
  - Coxcomb Chart
  - Polar Area Chart
  - Florence Nightingale Chart
chart_type: nightingale-rose-chart
category: part-to-whole
data_types:
  - categorical
  - continuous
  - time-series
data_contexts:
  - Renewable Energy & Transition
  - Energy Markets
complexity: medium
audience:
  - media
  - technical
visual_styles:
  - artistic
  - editorial
color_approach: sequential
libraries:
  - d3
  - echarts
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/composition
  - data-type/categorical
  - data-type/cyclical
  - data-type/proportional
  - complexity/intermediate
  - audience/analyst
  - audience/general-public
  - audience/policymaker
  - theme/energy
  - theme/climate
  - theme/renewable-energy
---

# Nightingale Rose Chart

## What It Is
A Nightingale rose chart divides a circle into sectors of equal angular width, where each sector's radius (and therefore area) varies to represent a value. Unlike a [[Pie Chart]] where the angle encodes value, here the angle is fixed and the radius does the encoding. Invented by Florence Nightingale to illustrate causes of mortality in the Crimean War, it remains one of the most historically significant statistical graphics and is effective for cyclical or categorical data with a visual impact that exceeds a standard [[Bar Chart]].

## Best Data Types
- Categorical data with 6-12 categories of roughly similar scale
- Cyclical data (months, seasons, compass directions)
- Proportional data where area comparison is acceptable
- Single-measure breakdowns across categories

## When to Use
- Showing monthly or seasonal patterns in a visually striking circular format
- Presenting categorical breakdowns where the circular layout reinforces periodicity
- Creating visually memorable charts for reports and presentations
- When a [[Bar Chart]] is technically correct but lacks visual distinction
- Comparing magnitudes across equal-angle sectors

## When NOT to Use
> [!warning] Avoid When
> - Precise area comparison is critical (area perception is less accurate than length)
> - Categories have no natural circular ordering
> - You have more than 12 or fewer than 4 categories
> - Multiple series need comparison (overlapping roses are hard to read)
> - The audience needs to extract exact values

## Real-World Use Cases
- Florence Nightingale's original mortality cause diagram (the chart that invented this type)
- Seasonal sales patterns in retail analytics
- Crime statistics by month of year
- Weather patterns by compass direction

### Energy & Climate Applications
- Monthly emission volumes showing seasonal heating and cooling demand patterns
- Cause-of-emission breakdown: combustion, process, fugitive, purchased energy as rose sectors
- Renewable generation by month revealing solar/wind seasonal complementarity
- Wind energy potential by compass direction (related to but distinct from wind rose)
- Carbon credit retirement volumes by quarter showing market seasonality

## Visual Style Variations
- **Classic Nightingale** — equal-angle sectors, varying radius, single color gradient
- **Stacked rose** — concentric layers within each sector showing composition
- **Multi-ring** — overlapping roses for two series comparison (use sparingly)
- **Labeled sectors** — category labels at each sector with value annotations

## Related Charts
- [[Pie Chart]] — angle encodes value (vs. radius in rose chart); less visually dramatic
- [[Radial Bar Chart]] — bars extend from center; encodes length not area
- [[Radar Chart]] — connected line across axes; shows multi-metric profile not composition

## Tools That Support This
- **D3.js** — polar area layout with full customization
- **ECharts** — built-in Nightingale rose option in pie chart configuration
- **Datylon** — publication-quality rose chart templates

## Inspiration Sources
- [ECharts Nightingale Rose](https://echarts.apache.org/examples/en/editor.html?c=pie-roseType) — interactive rose chart examples
- [Florence Nightingale's Statistical Graphics](https://www.sciencemuseum.org.uk/objects-and-stories/florence-nightingale-pioneer-statistician) — historical context and original diagrams
