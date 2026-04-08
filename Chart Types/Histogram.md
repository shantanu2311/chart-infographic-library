---
title: Histogram
aliases:
  - Frequency Histogram
  - Frequency Distribution Chart
chart_type: histogram
category: distribution
data_types:
  - continuous
data_contexts:
  - Carbon Markets
  - Energy Markets
  - Climate & Emissions
complexity: medium
audience:
  - technical
  - academic
visual_styles:
  - minimal
  - corporate
color_approach: sequential
libraries:
  - d3
  - plotly
  - chartjs
  - matplotlib
  - recharts
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/distribution
  - data-type/continuous-numeric
  - complexity/intermediate
  - audience/analyst
  - audience/researcher
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/energy-markets
  - theme/climate
  - theme/iea
---

# Histogram

## What It Is
A histogram groups continuous numeric data into equal-width bins and uses the height of each bar to show the frequency (or density) of observations falling within that range. Unlike a [[Bar Chart]] where each bar represents a discrete category, histogram bars represent contiguous ranges of a continuous variable and are drawn without gaps. It is the foundational chart for understanding the shape, centre, spread, and skewness of a data distribution.

## Best Data Types
- Continuous numeric data (prices, temperatures, intensities, durations)
- Large datasets where individual data points are too numerous to display
- Measurement data from sensors, instruments, or models
- Financial data (returns, prices, costs) where distribution shape matters
- Any variable where understanding frequency across a range is the goal

## When to Use
- Exploring the distribution of a single continuous variable
- Checking for normality, skewness, or bimodality in data before analysis
- Identifying outliers and understanding data spread
- Comparing distributions side by side when using small multiples
- Communicating how frequently values fall within specific ranges

## When NOT to Use
> [!warning] Avoid When
> - Data is categorical or discrete with few values (use a [[Bar Chart]])
> - You need to compare distributions across many groups simultaneously (use a [[Box Plot]] or [[Violin Plot]])
> - The dataset is very small (under 30 observations), where individual data points are more informative
> - You want to show the cumulative distribution (use an empirical CDF plot)
> - Bin width selection would materially change the story (consider a [[Density Plot]] for a smoother representation)

## Real-World Use Cases
- Distribution of student test scores in an education report
- Frequency of daily stock returns for risk analysis
- Age distribution of a survey population
- Response time distribution for a web service

### Energy & Climate Applications
- Distribution of carbon credit prices across thousands of transactions in voluntary markets (Verra, Gold Standard registry data)
- Solar irradiance frequency distribution across monitoring stations for site selection (Global Solar Atlas data)
- Facility-level emission intensity distribution within Indian iron and steel sub-sectors (BEE PAT data)
- Distribution of hourly electricity spot prices in a deregulated market (IEX India, NordPool)
- Wind speed frequency distribution at prospective turbine sites (essential for capacity factor estimation)

## Visual Style Variations
- **Standard histogram** — equal-width bins with frequency on y-axis; the most common format
- **Normalised histogram** — y-axis shows probability density instead of count, allowing comparison across datasets of different sizes
- **Overlapping histograms** — two distributions plotted on the same axes with transparency for direct comparison
- **Cumulative histogram** — bars show running total, building up to the full count or 100%

## Related Charts
- [[Density Plot]] — a smoothed version of the histogram that eliminates binning artefacts
- [[Box Plot]] — summarises the distribution with five statistics; much more compact
- [[Bar Chart]] — visually similar but for categorical data; the key distinction is discrete vs continuous
- [[Violin Plot]] — combines density plot shape with box plot statistics for richer distribution display

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Global Solar Atlas](https://globalsolaratlas.info/) — solar irradiance data and distribution visualisations
- [IEA Energy Statistics](https://www.iea.org/data-and-statistics) — energy price and generation distribution data
