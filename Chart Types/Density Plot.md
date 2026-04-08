---
title: Density Plot
aliases:
  - KDE Plot
  - Kernel Density Estimate
  - Density Curve
chart_type: density-plot
category: distribution
data_types:
  - continuous
data_contexts:
  - Renewable Energy & Transition
  - Climate & Emissions
  - Energy Markets
complexity: medium
audience:
  - technical
  - academic
visual_styles:
  - minimal
  - editorial
color_approach: sequential
libraries:
  - d3
  - plotly
  - matplotlib
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/distribution
  - data-type/continuous-numeric
  - data-type/large-datasets
  - complexity/intermediate
  - audience/analyst
  - audience/researcher
  - audience/data-scientist
  - theme/renewable-energy
  - theme/energy-markets
  - theme/climate
  - theme/iea
  - theme/carbon-markets
---

# Density Plot

## What It Is
A density plot uses kernel density estimation (KDE) to create a smooth, continuous curve representing the probability density function of a dataset. Instead of binning data into discrete bars like a [[Histogram]], it places a small smooth kernel (typically Gaussian) at each data point and sums them to produce a continuous estimate of the underlying distribution. The area under the curve integrates to 1, making it easy to interpret as a probability distribution and to overlay multiple distributions for direct comparison.

## Best Data Types
- Continuous numeric data with large sample sizes (100+ observations)
- Data where the underlying distribution shape is of primary interest
- Multiple groups or conditions that need to be compared on the same axis
- Time-series values aggregated for distributional analysis
- Measurement data from sensors, simulations, or statistical models

## When to Use
- Comparing the distribution shapes of two or more groups on the same axes
- When you want a smoother, less noisy alternative to a histogram
- Overlaying multiple distributions to identify shifts, overlaps, or separations
- Exploring data to detect multimodality, skewness, or heavy tails
- Creating probability-based visualisations for forecasting or risk analysis

## When NOT to Use
> [!warning] Avoid When
> - Sample size is small (under 30 observations), where the kernel estimate is unreliable
> - The audience is non-technical and may not understand what the y-axis (density) represents
> - Exact bin counts or frequencies are needed (use a [[Histogram]])
> - Data is discrete, ordinal, or categorical (KDE creates misleading smooth curves between discrete values)
> - Bandwidth selection is critical and a poor choice could hide or fabricate features in the distribution

## Real-World Use Cases
- Distribution of daily stock returns for portfolio risk assessment
- Comparing height or weight distributions across populations
- Response time distributions for two versions of a software system (A/B test)
- Rainfall amount distributions across climate zones

### Energy & Climate Applications
- Solar generation probability curves for different regions and seasons (essential for grid integration planning and storage sizing)
- Emission factor distributions across fuel types and measurement methods (showing uncertainty in GHG accounting)
- Temperature anomaly distributions by decade from IPCC climate model ensembles (showing how the distribution shifts and widens over time)
- Wind resource assessment: overlaying wind speed density curves for multiple candidate sites on one chart
- Carbon credit price density overlays for different project types (nature-based vs technology-based vs avoidance)

## Visual Style Variations
- **Single density curve** — one smooth line with optional fill showing the distribution of a single variable
- **Overlapping densities** — multiple semi-transparent filled curves on the same axes for group comparison
- **Stacked density** — densities stacked vertically showing composition (less common, harder to read)
- **Density with rug plot** — individual observations shown as tick marks along the x-axis beneath the curve for sample size transparency

## Related Charts
- [[Histogram]] — the binned precursor; more intuitive for some audiences but noisier
- [[Violin Plot]] — mirrors the density curve on both sides of a central axis, often combined with a box plot
- [[Ridgeline Plot]] — stacks multiple density curves vertically with slight overlap for elegant temporal or categorical comparison
- [[Box Plot]] — a much more compact summary that sacrifices distribution shape detail

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IPCC AR6 Working Group I](https://www.ipcc.ch/report/ar6/wg1/) — temperature anomaly distribution visualisations
- [Claus Wilke — Fundamentals of Data Visualization](https://clauswilke.com/dataviz/) — excellent chapter on density plots and distribution visualisation
