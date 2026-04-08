---
title: Line Chart
aliases:
  - Line Graph
  - Time Series Chart
  - Trend Chart
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/continuous
  - data-type/quantitative
  - complexity/beginner
  - audience/executive
  - audience/analyst
  - audience/policymaker
  - audience/general-public
  - theme/energy-markets
  - theme/climate
  - theme/finance
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/net-zero
  - theme/iea
category: Temporal
complexity: beginner
best_audience: executives, analysts, policymakers, general public
---

# Line Chart

## What It Is
A line chart plots data points connected by straight line segments along a continuous axis, almost always time on the horizontal axis and a quantitative measure on the vertical axis. It is the most fundamental and widely understood chart type for showing trends, patterns, and rates of change over time. Multiple lines on the same chart enable direct comparison of trends across categories.

## Best Data Types
- Time series data with regular or irregular intervals
- Continuous quantitative measurements over an ordered dimension
- Projected or forecasted values alongside historical actuals
- Multiple series for trend comparison (up to ~7 lines before clutter)

## When to Use
- Showing how a value changes over time (the most common use case in data visualization)
- Comparing trends across multiple categories on a shared time axis
- Highlighting inflection points, accelerations, or decelerations
- Presenting projections, scenarios, or targets alongside historical data
- Communicating simple trends to any audience, including non-technical stakeholders

## When NOT to Use
> [!warning] Avoid When
> - The data is categorical with no inherent order — use a [[Bar Chart]]
> - You want to emphasize the magnitude or volume under the curve — use an [[Area Chart]]
> - You have too many series (more than ~7) creating spaghetti — consider a [[Bump Chart]] or small multiples
> - The data has very few points (fewer than 4) — a [[Bar Chart]] or [[Slope Chart]] may be clearer
> - You need to show the composition of a total — use a [[Stacked Bar Chart]] or [[Area Chart]]

## Real-World Use Cases
- Stock price movements over trading sessions
- Population growth over decades
- Monthly website traffic trends
- GDP growth rate comparisons across countries

### Energy & Climate Applications
- **Global Temperature Anomaly Trends**: NASA GISS or HadCRUT datasets showing deviation from pre-industrial baseline, the most iconic climate chart
- **Carbon Price Evolution**: EU ETS European Union Allowance (EUA) prices from inception through Phase IV, showing the impact of market stability reserve and policy tightening
- **Renewable Capacity Growth Curves**: Global installed capacity for solar PV, onshore wind, offshore wind, and battery storage over the past two decades
- **IEA Net-Zero Pathway Projections**: Historical emissions versus NZE 2050, APS, and STEPS scenario lines from IEA World Energy Outlook
- **Electricity Demand Forecasts**: National or regional electricity demand projections under different economic growth and electrification assumptions
- **Levelized Cost of Energy (LCOE) Decline**: Solar PV and wind LCOE trajectories from 2010 to present, demonstrating learning curve effects

## Visual Style Variations
- **Single line with annotation**: one series with key events or milestones annotated directly on the chart
- **Multi-line comparison**: 3-5 series with distinct colors and a clear legend
- **Line with confidence band**: a central trend line with a shaded uncertainty range (common in projections)
- **Sparkline**: a minimalist, small-scale line chart embedded inline in text or tables for at-a-glance trends

## Related Charts
- [[Area Chart]] — a line chart with the area below filled, emphasizing magnitude and volume
- [[Bump Chart]] — shows ranking changes over time rather than absolute values, reducing spaghetti effect
- [[Scatter Plot]] — when the relationship between two variables (not necessarily time) is the focus

## Inspiration Sources
- [NASA GISS Surface Temperature Analysis](https://data.giss.nasa.gov/gistemp/) — the canonical global temperature anomaly line chart
- [IEA World Energy Outlook](https://www.iea.org/reports/world-energy-outlook-2023) — scenario-based energy projections with multiple pathway lines
- [IRENA Renewable Power Generation Costs](https://www.irena.org/Publications) — LCOE trend lines by technology
- [EMBER Global Electricity Review](https://ember-climate.org/insights/research/global-electricity-review-2024/) — electricity generation trends by source
- [Carbon Brief Interactive Charts](https://www.carbonbrief.org/) — annotated climate data line charts with excellent storytelling
