---
title: Column Chart
aliases:
  - Vertical Bar Chart
tags:
  - chart-type/comparison
  - data-type/categorical
  - data-type/numeric
  - data-type/time-series
  - complexity/beginner
  - audience/general
  - audience/executive
  - audience/analyst
  - theme/energy-markets
  - theme/climate
  - theme/carbon-markets
  - theme/mdb
  - theme/public-finance
category: Comparison
complexity: beginner
best_audience: general, executive, analyst
---

# Column Chart

## What It Is
A column chart uses vertical rectangular bars to compare values across categories, with the height of each bar proportional to the data value. It is the vertical counterpart to the [[Bar Chart]] and is particularly effective when the x-axis represents ordered categories such as time periods or sequential stages. Column charts are among the most commonly used visualisations in business and policy reporting.

## Best Data Types
- Categorical data with numeric values where categories have a natural order
- Time-based categories (years, quarters, months) with discrete measurements
- Small-to-medium number of categories (typically 3-15)
- Grouped or stacked sub-categories for composition analysis
- Budget or financial period data

## When to Use
- Comparing values across time periods (annual emissions, quarterly disbursements)
- When the x-axis categories are short labels (years, codes, abbreviations)
- Showing discrete snapshots rather than continuous trends
- Presenting grouped comparisons (e.g., fuel types across years)
- When the audience expects a conventional chart format

## When NOT to Use
> [!warning] Avoid When
> - Category labels are long (use a [[Bar Chart]] instead for readability)
> - You have more than 15-20 categories (the chart becomes cluttered)
> - You need to show continuous trends (a line chart is more effective)
> - You are comparing a single value to a target (use a [[Bullet Chart]])
> - Data varies by orders of magnitude (consider a log scale or different chart type)

## Real-World Use Cases
- Quarterly revenue comparison across fiscal years
- Monthly website traffic by channel
- Voter turnout by election cycle
- Product sales by region and quarter

### Energy & Climate Applications
- Annual electricity generation by fuel type (coal, gas, nuclear, solar, wind, hydro) from IEA Electricity Information
- Carbon price by exchange (EU ETS, UK ETS, RGGI, California, Korea) at a point in time
- Quarterly MDB climate finance disbursements (World Bank IDA/IBRD, GCF, CIF)
- Year-over-year growth in global solar PV and wind capacity additions (IRENA data)
- UNFCCC Nationally Determined Contribution submissions by year and ambition tier

## Visual Style Variations
- **Stacked column chart** — segments within each column show composition (e.g., Scope 1 + 2 + 3 stacking to total emissions per year)
- **Grouped column chart** — side-by-side columns within each category for direct sub-group comparison
- **Waterfall column chart** — columns connected to show cumulative effect of sequential positive and negative values
- **Column chart with reference line** — a horizontal line indicating a target, average, or benchmark (e.g., 1.5C pathway threshold)

## Related Charts
- [[Bar Chart]] — horizontal orientation; better for long labels and many categories
- [[Stacked Bar Chart]] — composition focus with part-to-whole breakdown
- [[Area Chart]] — fills the space under a line to emphasise volume over time
- [[Waterfall Chart]] — shows how an initial value is affected by sequential changes

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IRENA Data & Statistics](https://www.irena.org/Data) — renewable energy column chart examples
- [World Bank Open Data](https://data.worldbank.org/) — development finance visualisations
