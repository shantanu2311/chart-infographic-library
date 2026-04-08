---
title: Stacked Bar Chart
aliases:
  - Stacked Column Chart
  - Segmented Bar Chart
chart_type: stacked-bar-chart
category: composition
data_types:
  - categorical
  - continuous
  - time-series
data_contexts:
  - Energy Markets
  - Renewable Energy & Transition
  - Public Finance & MDBs
  - Ember Global Electricity Data
complexity: medium
audience:
  - executive
  - technical
  - policymaker
visual_styles:
  - corporate
  - minimal
  - dashboard
  - editorial
color_approach: categorical
libraries:
  - d3
  - plotly
  - chartjs
  - echarts
  - recharts
  - matplotlib
  - highcharts
  - flourish
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/composition
  - data-type/categorical
  - data-type/multi-series
  - data-type/temporal
  - complexity/intermediate
  - audience/analysts
  - audience/policy-makers
  - audience/executives
  - theme/energy-mix
  - theme/emissions
  - theme/MDBs
  - theme/energy-transition
---

# Stacked Bar Chart

## What It Is
A stacked bar chart extends the standard bar chart by dividing each bar into segments representing sub-categories. Each segment's length is proportional to its value, and the total bar length represents the aggregate. It is one of the most versatile composition charts, capable of showing both the total and its breakdown across groups or over time. Bars can be oriented vertically (column) or horizontally.

## Best Data Types
- Categorical data with multiple series that sum to a meaningful total
- Time-series composition (e.g., energy mix by year)
- Cross-group comparisons with sub-category breakdowns
- Up to 5-7 series stacked within each bar

## When to Use
- Comparing totals across groups while also showing their internal composition
- Tracking how composition changes over time (e.g., shifting energy mix by decade)
- Showing part-to-whole relationships across multiple entities (countries, facilities, sectors)
- When you need both absolute values and proportional breakdown in one view
- Comparing Scope 1 + Scope 2 + Scope 3 across multiple facilities or years

## When NOT to Use
> [!warning] Avoid When
> - You have more than 7 stacked series (middle segments become hard to compare across bars)
> - Comparing individual segment values across bars is the primary goal (only the bottom segment shares a common baseline)
> - The data is not additive or does not represent parts of a whole
> - A 100% stacked bar would mislead because absolute totals vary dramatically and matter
> - Precision in individual segment comparison is critical (use grouped bars instead)

## Real-World Use Cases
- Revenue breakdown by product line across quarters
- Population by age group across countries
- Project portfolio: tasks by status (complete, in-progress, pending) across teams
- Website traffic by channel (organic, paid, social, direct) over months

### Energy & Climate Applications
- National energy mix by country: coal, gas, oil, nuclear, hydro, solar, wind stacked per country
- Scope 1 + Scope 2 + Scope 3 emissions stacked per facility or reporting period
- MDB climate lending by sector (energy, transport, agriculture) and instrument (grants, loans, equity)
- Electricity generation mix evolution: stacked fuels over decades showing the energy transition
- Climate finance commitments by source (bilateral, multilateral, private) stacked per year

## Visual Style Variations
- **Standard stacked** — absolute values, total bar height reflects magnitude
- **100% stacked** — all bars normalized to 100%, emphasizing proportional composition
- **Horizontal stacked** — bars run left-to-right, better for long category labels
- **Diverging stacked** — bars extend in both directions from a center axis (e.g., positive/negative contributions)

## Related Charts
- [[Bar Chart]] — use when you only need to compare totals without sub-category breakdown
- [[Marimekko Chart]] — extends the stacked bar by also varying bar width to encode a second dimension
- [[Area Chart]] — continuous version of a stacked bar for time-series data with many time points

## Inspiration Sources
- [IEA Data and Statistics](https://www.iea.org/data-and-statistics) — energy mix stacked bars by country and year
- [World Resources Institute Climate Data Explorer](https://www.climatewatchdata.org/) — emissions by sector stacked over time
- [World Bank Joint MDB Climate Finance Report](https://www.worldbank.org/en/topic/climatechange) — lending by sector and instrument
