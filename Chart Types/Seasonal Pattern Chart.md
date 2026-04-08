---
title: Seasonal Pattern Chart
aliases:
  - Monthly Pattern Chart
  - Seasonality Chart
  - Year-over-Year Monthly Chart
  - Cyclical Pattern Chart
chart_type: seasonal-pattern-chart
category: temporal
data_types:
  - time-series
  - continuous
data_contexts:
  - Energy Markets
  - Renewable Energy & Transition
  - Ember Global Electricity Data
complexity: medium
audience:
  - technical
  - policymaker
visual_styles:
  - minimal
  - dashboard
  - editorial
color_approach: sequential
libraries:
  - d3
  - plotly
  - flourish
  - matplotlib
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/monthly
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - theme/energy-markets
  - theme/renewable-energy
  - theme/climate
---

# Seasonal Pattern Chart

## What It Is
A visualization showing monthly or seasonal patterns by overlaying multiple years on the same 12-month axis (Jan-Dec). Rather than a continuous time series, it decomposes data into its seasonal cycle, allowing year-over-year comparison at each month. Ember uses this as their third data explorer tab ("Seasonal patterns"), showing how monthly electricity generation patterns shift across years.

## Best Data Types
- Monthly or quarterly data spanning multiple years
- Data with strong seasonal cycles (temperature, energy demand, renewable generation)
- Year-over-year comparisons at sub-annual granularity
- Cyclical metrics where the seasonal pattern itself is the insight

## When to Use
- Identifying seasonal patterns in energy generation, demand, or prices
- Comparing "this year's January" against previous years' Januaries
- Detecting whether seasonal patterns are shifting (earlier summers, longer winters)
- Showing when peak demand or peak generation occurs and how it's changing
- Revealing anomalies: months that deviate from the normal seasonal pattern

## When NOT to Use
> [!warning] Avoid When
> - Long-term trend is more important than seasonality (use a continuous line chart)
> - Data doesn't have meaningful seasonal variation
> - Too many years overlap making the chart unreadable (limit to 4-5 years or use highlighting)
> - Monthly resolution is insufficient (need daily or hourly patterns)

## Real-World Use Cases
- Retail sales seasonal patterns (holiday peaks, summer dips)
- Tourism arrivals by month across years
- Agricultural production cycles
- Hospital admissions seasonal variation

### Energy & Climate Applications
- **Ember's seasonal patterns tab**: Electricity generation by month showing summer solar peaks, winter demand peaks
- **Grid operator load curves**: Monthly electricity demand showing summer cooling vs winter heating peaks
- **Solar generation seasonality**: Monthly GWh comparing 2020-2025, showing both growth and seasonal shape
- **Hydropower seasonality**: Monsoon-driven hydro generation peaks (critical for India, Brazil)
- **Carbon price seasonality**: EUA prices often dip in summer, rise in winter — overlay years to see pattern
- **Wind capacity factor**: Monthly wind output showing winter peaks in northern Europe
- **Temperature anomaly by month**: Monthly temperatures overlaid across decades showing warming trend within seasonal cycle

## Visual Style Variations
- **Multi-year spaghetti plot** — each year as a separate colored line on Jan-Dec axis, latest year highlighted
- **Highlighted current year** — all historical years in light grey, current year in bold color
- **Seasonal band** — min/max/median band from historical years, with current year overlaid
- **Small multiples by year** — 12-month chart repeated for each year in a grid
- **Polar/radial layout** — months arranged in a circle, years as concentric rings

## Related Charts
- [[Line Chart]] — continuous time series without the seasonal decomposition
- [[Heatmap]] — months as rows, years as columns, intensity as color (alternative encoding)
- [[Ridgeline Plot]] — monthly distributions stacked vertically
- [[Radial Bar Chart]] — circular layout for cyclical monthly data
- [[Small Multiples]] — same monthly chart repeated per year or per region

## Tools That Support This
- Flourish (Ember's implementation)
- D3.js (custom year-overlay)
- ggplot2 (facet_wrap by month or color by year)
- Datawrapper

## Inspiration Sources
- [Ember Electricity Data Explorer — Seasonal patterns tab](https://ember-energy.org/data/electricity-data-explorer/) — the canonical implementation
- [Our World in Data — CO2 Emissions Seasonality](https://ourworldindata.org/co2-emissions) — monthly emission patterns
- [Electricity Map](https://app.electricitymap.org/) — real-time grid generation with seasonal context
