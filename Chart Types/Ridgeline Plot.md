---
title: Ridgeline Plot
aliases:
  - Joy Plot
  - Ridge Plot
  - Joyplot
chart_type: ridgeline-plot
category: distribution
data_types:
  - continuous
  - time-series
data_contexts:
  - Climate & Emissions
  - Energy Markets
complexity: complex
audience:
  - technical
  - academic
  - media
visual_styles:
  - editorial
  - artistic
  - data-journalism
color_approach: sequential
libraries:
  - d3
  - plotly
  - matplotlib
  - vega
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/distribution
  - data-type/distributions-over-time
  - data-type/continuous-numeric
  - data-type/grouped
  - complexity/advanced
  - audience/analyst
  - audience/researcher
  - audience/data-scientist
  - theme/climate
  - theme/energy-markets
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/iea
  - theme/net-zero
---

# Ridgeline Plot

## What It Is
A ridgeline plot (originally called a joy plot, after the Joy Division album cover) displays multiple density distributions stacked vertically with slight overlap, creating a mountain-ridge-like visual effect. Each row represents a different group or time period, and the overlapping arrangement allows efficient comparison of how distribution shapes evolve across categories or over time. It is one of the most visually striking ways to show distributional change, combining compactness with rich detail.

## Best Data Types
- Continuous numeric data distributed across ordered categories (time periods, sequential groups)
- Time-series data where you want to compare the distribution shape at each time slice
- Seasonal or cyclical data where periodic patterns are expected
- Multiple groups (8-30+) that need distributional comparison without faceting into separate charts
- Large datasets where each group has enough observations (50+) for reliable density estimation

## When to Use
- Showing how a distribution shifts, spreads, or changes shape over time
- Comparing seasonal patterns across months, quarters, or years
- Displaying the evolution of a measurement across sequential categories
- When you have many groups and a [[Violin Plot]] or overlay of [[Density Plot]]s would be too cluttered
- Creating visually compelling data storytelling in presentations or reports

## When NOT to Use
> [!warning] Avoid When
> - You need precise value reading (the overlapping layout makes exact density comparisons difficult)
> - Sample sizes per group are small (under 30), producing unreliable density estimates
> - The categories have no natural order (the stacked layout implies sequence)
> - You have fewer than 5 groups (simpler alternatives like overlapping density plots work better)
> - The audience is unfamiliar with density plots and may struggle to interpret the y-axis
> - Distributions are very similar across groups (the chart will look uniform and uninformative)

## Real-World Use Cases
- Monthly temperature distributions across 12 months for a climate station
- Song duration distributions across decades of music (the famous Joy Division-inspired example)
- Wait time distributions by hour of day for a service centre
- Earthquake magnitude distributions by decade

### Energy & Climate Applications
- Monthly electricity demand distributions for grid planning (showing how the demand curve shape changes from winter to monsoon to summer in India)
- Temperature anomaly shifts decade by decade from pre-industrial to present (IPCC, NASA GISS, or HadCRUT data)
- Carbon price evolution: distribution of daily closing prices by year for the EU ETS showing progressive tightening and volatility changes
- Solar generation hourly profiles by month (showing how the generation curve narrows in winter and broadens in summer)
- Wind speed distributions by month at a candidate turbine site (revealing seasonal resource variability for capacity planning)

## Visual Style Variations
- **Standard ridgeline** — partially overlapping density curves with consistent fill colour and slight transparency
- **Gradient-filled ridgeline** — fill colour mapped to a variable (e.g., warmer colours for higher median values) to encode a second dimension
- **Ridgeline with quantile lines** — vertical lines within each density marking the median and quartiles
- **Mirrored ridgeline** — densities extend both above and below the baseline for a symmetric effect (less common, visually striking)

## Related Charts
- [[Density Plot]] — the building block of the ridgeline; a single smooth distribution curve
- [[Stream Graph]] — a related chart that shows composition over time using flowing, stacked shapes
- [[Violin Plot]] — shows mirrored density for group comparison but arranged horizontally rather than stacked vertically
- [[Box Plot]] — the compact statistical summary alternative when distribution shape detail is secondary

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Claus Wilke — Fundamentals of Data Visualization](https://clauswilke.com/dataviz/) — ridgeline plot chapter with climate and temporal examples
- [NASA GISS Surface Temperature Analysis](https://data.giss.nasa.gov/gistemp/) — temperature anomaly data ideal for ridgeline visualisation
