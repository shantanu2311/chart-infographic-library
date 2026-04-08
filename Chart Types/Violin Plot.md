---
title: Violin Plot
aliases:
  - Violin Chart
  - Density Box Plot
chart_type: violin-plot
category: distribution
data_types:
  - continuous
  - categorical
data_contexts:
  - Renewable Energy & Transition
  - Climate & Emissions
complexity: complex
audience:
  - technical
  - academic
visual_styles:
  - minimal
  - editorial
color_approach: categorical
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
  - data-type/continuous-numeric
  - data-type/grouped
  - complexity/advanced
  - audience/analyst
  - audience/researcher
  - audience/data-scientist
  - theme/renewable-energy
  - theme/energy-markets
  - theme/carbon-markets
  - theme/climate
  - theme/finance
---

# Violin Plot

## What It Is
A violin plot combines a [[Box Plot]] with a mirrored [[Density Plot]] (kernel density estimate) on each side, creating a shape that resembles a violin. The width of the "violin" at any point represents the density of data at that value, revealing the full distribution shape including bimodality, skewness, and clustering that a box plot alone would hide. It provides both the statistical summary of a box plot and the distributional detail of a density plot in one compact visualisation.

## Best Data Types
- Continuous numeric data across multiple groups where distribution shape matters
- Datasets large enough (50+ observations per group) to produce meaningful density estimates
- Data with potentially complex distributions (bimodal, multimodal, skewed)
- Comparative analysis where understanding the full probability density is important
- Performance, measurement, or price data where variability patterns differ across groups

## When to Use
- Comparing distributions across groups when box plots lose too much information
- Revealing bimodality or multimodality hidden by simpler summary charts
- Academic, research, or technical reports where the audience understands density estimation
- Exploring data before hypothesis testing to understand distributional assumptions
- When the shape of the distribution is the story, not just the central tendency

## When NOT to Use
> [!warning] Avoid When
> - The audience is non-technical or unfamiliar with density plots and distribution concepts
> - Sample sizes are small (under 30 per group), where density estimates become unreliable and misleading
> - You need a quick, scannable overview (a [[Box Plot]] is more compact and familiar)
> - There are many groups to compare (beyond 8-10 violins, the chart becomes crowded)
> - The data is discrete or categorical (density estimation on discrete data creates artefacts)
> - A simpler chart (histogram, box plot) already tells the complete story

## Real-World Use Cases
- Gene expression levels across tissue types in genomics research
- Response time distributions by server configuration in performance benchmarking
- Student grade distributions across courses or professors
- Property price distributions by neighbourhood in real estate analysis

### Energy & Climate Applications
- Wind speed distributions across candidate sites for turbine installation (revealing bimodal wind patterns at some locations)
- Carbon price distribution across compliance markets (EU ETS, UK ETS, Korea ETS, RGGI) showing different volatility profiles
- Energy poverty metrics distribution across states (percentage of household income spent on energy, comparing urban vs rural)
- Hourly electricity demand distributions by season for grid planning (revealing peak and off-peak clustering)
- Solar capacity factor distributions across geographic regions (showing how cloud cover creates different generation profiles)

## Visual Style Variations
- **Standard violin** — symmetric mirrored density with embedded box plot showing median and IQR
- **Half violin** — density on one side only, combined with jittered points on the other side for transparency
- **Split violin** — two halves show different sub-groups (e.g., male/female, 2020/2025) for direct within-category comparison
- **Bean plot** — a variant where individual observations are shown as small horizontal lines within the density shape

## Related Charts
- [[Box Plot]] — the compact statistical summary that the violin plot extends with full distribution detail
- [[Density Plot]] — the underlying smoothed distribution curve; a violin is essentially two mirrored density plots
- [[Ridgeline Plot]] — an alternative for comparing many distributions that stacks density curves vertically
- [[Histogram]] — the binned precursor to the density plot; less smooth but sometimes more interpretable

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Hintze & Nelson (1998) — Violin Plots: A Box Plot-Density Trace Synergism](https://doi.org/10.1080/00031305.1998.10480559) — the original violin plot paper
- [Global Wind Atlas](https://globalwindatlas.info/) — wind speed distribution data for renewable energy site assessment
