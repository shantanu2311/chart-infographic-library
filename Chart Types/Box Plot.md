---
title: Box Plot
aliases:
  - Box & Whisker Plot
  - Box-and-Whisker Chart
tags:
  - chart-type/distribution
  - data-type/continuous-numeric
  - data-type/grouped
  - complexity/intermediate
  - audience/analyst
  - audience/researcher
  - theme/energy-markets
  - theme/renewable-energy
  - theme/climate
  - theme/carbon-markets
  - theme/iea
  - theme/public-finance
category: Distribution
complexity: intermediate
best_audience: analyst, researcher
---

# Box Plot

## What It Is
A box plot (or box-and-whisker plot) displays the five-number summary of a dataset: minimum, first quartile (Q1), median (Q2), third quartile (Q3), and maximum. The box spans the interquartile range (IQR = Q3 - Q1), a line inside the box marks the median, and whiskers extend to the most extreme data points within 1.5x IQR of the box edges. Points beyond the whiskers are plotted individually as outliers. It provides a compact, standardised summary of distribution shape, central tendency, spread, and outliers.

## Best Data Types
- Continuous numeric data distributed across groups or categories
- Datasets where comparing central tendency and spread across groups is the goal
- Data with potential outliers that need identification
- Time-series data grouped by period (monthly, quarterly, yearly)
- Any measurement data where understanding variability is critical

## When to Use
- Comparing distributions across multiple groups in a compact format
- Identifying outliers and understanding data spread at a glance
- Summarising large datasets where individual data points are impractical to show
- Statistical reporting where the five-number summary is meaningful
- Quality control and process monitoring (control chart alternative)

## When NOT to Use
> [!warning] Avoid When
> - The audience is non-technical and unfamiliar with quartiles and IQR concepts
> - You need to see the full shape of the distribution (use a [[Violin Plot]] or [[Density Plot]])
> - The dataset is very small (under 20 points per group), where the five-number summary can be misleading
> - You want to show bimodality or complex distribution shapes (box plots hide these)
> - Only comparing means or totals is needed (a [[Bar Chart]] with error bars is simpler)

## Real-World Use Cases
- Salary distributions across departments in an HR report
- Patient recovery times by treatment group in a clinical trial
- Manufacturing quality measurements across production lines
- Monthly temperature distributions for climate station comparisons

### Energy & Climate Applications
- Electricity price distribution by market (IEX India, NordPool, PJM, CAISO) showing median, spread, and extreme price spikes
- Emission factor ranges by grid region across India (Northern, Western, Southern, Eastern, North-Eastern grids from CEA data)
- LCOE spread by technology (solar PV, onshore wind, offshore wind, gas, coal) from IRENA or Lazard annual reports
- Carbon credit price distributions across project types in voluntary markets (renewable energy, forestry, cookstove, industrial gas)
- Annual MDB climate finance disbursement variability by recipient region (World Bank, ADB, AfDB historical data)

## Visual Style Variations
- **Standard box plot** — the classic five-number summary with outlier dots
- **Notched box plot** — notches at the median indicate confidence interval; if notches of two boxes do not overlap, medians are significantly different
- **Box plot with jittered points** — individual data points overlaid as jittered dots for sample size transparency
- **Grouped box plot** — multiple box plots per category for sub-group comparison (e.g., LCOE by technology and year)

## Related Charts
- [[Violin Plot]] — shows the full distribution shape alongside the box plot summary
- [[Histogram]] — provides more detail about distribution shape but for a single variable at a time
- [[Ridgeline Plot]] — displays multiple distributions stacked vertically for temporal or categorical comparison
- [[Density Plot]] — the smoothed distribution curve that a violin plot is based on

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IRENA Renewable Power Generation Costs](https://www.irena.org/publications) — LCOE box plot comparisons across technologies
- [John Tukey — Exploratory Data Analysis](https://en.wikipedia.org/wiki/Exploratory_data_analysis) — the origin of the box plot
