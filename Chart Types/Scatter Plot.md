---
title: Scatter Plot
aliases:
  - Scatter Chart
  - Scatter Graph
  - XY Plot
tags:
  - chart-type/relationship
  - data-type/continuous
  - data-type/bivariate
  - complexity/beginner
  - audience/analysts
  - audience/researchers
  - audience/policy-makers
  - theme/emissions
  - theme/renewable-energy
  - theme/energy-transition
  - theme/net-zero
category: Relationship
complexity: beginner
best_audience: analysts, researchers, policy-makers
---

# Scatter Plot

## What It Is
A scatter plot displays individual data points positioned along two continuous axes, revealing the relationship (or lack thereof) between two variables. Each point represents one observation, and the pattern of points reveals correlations, clusters, outliers, and distributions. It is the foundational chart type for exploring bivariate relationships and is often the first step in any quantitative analysis.

## Best Data Types
- Two continuous (numeric) variables measured for each observation
- Cross-sectional data (e.g., countries, companies, facilities measured at one point in time)
- Large datasets where patterns emerge from point density
- Data where outlier detection is important

## When to Use
- Exploring the relationship between two continuous variables (positive, negative, or no correlation)
- Identifying clusters, outliers, and distributional patterns in data
- Checking assumptions before running regression analysis
- Comparing entities (countries, companies) along two performance dimensions
- When the individual data points themselves are meaningful (not just the trend)

## When NOT to Use
> [!warning] Avoid When
> - One or both variables are categorical (use a [[Bar Chart]] or dot plot instead)
> - You have very few data points (fewer than 10), making pattern detection unreliable
> - Overplotting: too many points overlap and obscure the pattern (consider a [[Heatmap]] or hex-bin plot)
> - You need to show change over time for a single entity (use a [[Line Chart]])
> - Three or more variables need simultaneous display (use a [[Bubble Chart]] for a third variable)

## Real-World Use Cases
- Education: study hours (x) vs exam score (y) for students
- Real estate: square footage (x) vs sale price (y) for properties
- Biology: body mass (x) vs metabolic rate (y) across species
- Sports: player salary (x) vs performance metric (y)

### Energy & Climate Applications
- GDP per capita (x) vs CO2 emissions per capita (y) across countries (the Kaya identity visualization)
- Renewable energy investment (x) vs installed capacity deployment rate (y) by country
- Energy intensity (x) vs carbon intensity (y) for industrial facilities, identifying efficiency leaders
- Carbon price (x) vs emission reduction achieved (y) across jurisdictions with carbon pricing
- Wind speed (x) vs capacity factor (y) for wind farm site assessment

## Visual Style Variations
- **Standard scatter** — plain dots on two axes with optional trend line
- **Color-coded scatter** — dot color represents a categorical grouping (e.g., region, sector)
- **Regression overlay** — scatter with a fitted line and confidence band
- **Marginal distribution scatter** — histograms or density plots along each axis showing univariate distributions

## Related Charts
- [[Bubble Chart]] — extends scatter by encoding a third variable as bubble size
- [[Heatmap]] — bin-based alternative for very dense scatter patterns
- [[Line Chart]] — use when connecting data points in sequence (time-series) is meaningful

## Inspiration Sources
- [Gapminder](https://www.gapminder.org/tools/) — GDP vs life expectancy and emissions scatter plots
- [Our World in Data](https://ourworldindata.org/co2-emissions) — CO2 per capita vs GDP per capita
- [IEA Energy Efficiency Indicators](https://www.iea.org/data-and-statistics/data-tools/energy-efficiency-indicators) — energy and carbon intensity comparisons
