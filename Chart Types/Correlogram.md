---
title: Correlogram
aliases:
  - Correlation Matrix Chart
  - Correlation Heatmap
  - Pair Correlation Plot
chart_type: correlogram
category: relationship
data_types:
  - continuous
data_contexts:
  - Energy Markets
  - Commodity Markets (Oil Gas Metals)
  - ESG & Sustainable Finance
complexity: complex
audience:
  - technical
  - academic
visual_styles:
  - minimal
  - corporate
color_approach: diverging
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
  - chart-type/relationship
  - data-type/correlation
  - data-type/matrix
  - data-type/multivariate
  - complexity/advanced
  - audience/analysts
  - audience/researchers
  - audience/quants
  - theme/energy-markets
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/finance
---

# Correlogram

## What It Is
A correlogram is a specialized visualization of a correlation matrix, displaying pairwise correlation coefficients between multiple variables. It typically uses a combination of color intensity, shape size, or both to encode correlation strength and direction. Unlike a generic [[Heatmap]], a correlogram is purpose-built for statistical relationships, often incorporating significance indicators, hierarchical clustering, and upper/lower triangle optimizations to maximize information density.

## Best Data Types
- Correlation matrices (Pearson, Spearman, or Kendall) of multiple numeric variables
- Multivariate datasets where understanding inter-variable relationships is the goal
- Time-series cross-correlations between multiple signals
- Feature selection data in machine learning pipelines

## When to Use
- Exploring which variables in a multivariate dataset are related and how strongly
- Identifying multicollinearity before building regression or ML models
- Discovering unexpected relationships or confirming hypothesized correlations
- Summarizing the structure of a large set of variables in a single compact view
- Portfolio analysis: understanding co-movement of assets or risk factors

## When NOT to Use
> [!warning] Avoid When
> - You have fewer than 4 variables (a simple scatter matrix would be more informative)
> - The audience is non-technical and unfamiliar with correlation coefficients
> - You need to show causation, not just correlation (correlograms show association only)
> - The variables are categorical (correlation coefficients require continuous data)
> - More than 25-30 variables are included (the matrix becomes too large to read without clustering)

## Real-World Use Cases
- Finance: cross-asset correlation for portfolio diversification
- Psychology: correlation between survey instrument items for reliability analysis
- Manufacturing: process parameter correlations for quality control
- Climate science: correlations between temperature, precipitation, and vegetation indices

### Energy & Climate Applications
- Energy commodity price correlations: Brent crude, Henry Hub natural gas, Newcastle coal, EU ETS carbon, TTF gas across time windows
- ESG factor correlations: environmental score, social score, governance score vs financial performance metrics
- Weather variables vs renewable output: solar irradiance, wind speed, temperature, humidity vs solar PV and wind farm capacity factors
- Macroeconomic indicator correlations: GDP growth, energy demand, carbon emissions, renewable investment across countries
- Carbon market cross-correlations: EU ETS, UK ETS, RGGI, California cap-and-trade price co-movements

## Visual Style Variations
- **Color-only matrix** — cells colored by correlation value using a diverging palette (blue-white-red or similar)
- **Circle correlogram** — circle size encodes correlation magnitude, color encodes direction; half-matrix shown
- **Ellipse correlogram** — ellipse orientation and eccentricity encode correlation direction and strength
- **Mixed correlogram** — upper triangle shows circles/ellipses, lower triangle shows numeric values, diagonal shows variable distributions

## Related Charts
- [[Heatmap]] — the general-purpose matrix visualization; correlogram is a specialized subset
- [[Scatter Plot]] — shows the actual bivariate relationship for any single pair; use as a drill-down from correlogram
- [[Network Diagram]] — can represent strong correlations as edges between variable nodes for a graph-based view

## Inspiration Sources
- [R corrplot Package Documentation](https://cran.r-project.org/web/packages/corrplot/) — canonical correlogram styles and options
- [BloombergNEF](https://about.bnef.com/) — energy commodity correlation analyses
- [Carbon Pulse](https://carbon-pulse.com/) — carbon market price correlation reporting
