---
title: Change Attribution Chart
aliases:
  - Driver Decomposition Chart
  - Source Attribution Chart
  - Change Drivers Chart
  - Contribution Analysis Chart
chart_type: change-attribution-chart
category: specialized
data_types:
  - categorical
  - time-series
  - continuous
data_contexts:
  - Energy Markets
  - Renewable Energy & Transition
  - Climate & Emissions
  - Ember Global Electricity Data
complexity: medium
audience:
  - technical
  - policymaker
  - executive
visual_styles:
  - editorial
  - corporate
  - data-journalism
color_approach: diverging
libraries:
  - d3
  - flourish
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/specialized
  - data-type/categorical
  - data-type/time-series
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - theme/energy-markets
  - theme/renewable-energy
  - theme/climate
  - theme/iea
---

# Change Attribution Chart

## What It Is
A visualization that decomposes the total change in a metric into contributions from individual drivers or categories. Unlike a simple bar chart showing totals, it breaks down *what caused the change* — showing which sources drove an increase and which drove a decrease. Ember uses this as their "Change between years" tab, showing which electricity sources (coal, gas, solar, wind, etc.) contributed to generation changes between two periods.

## Best Data Types
- Year-over-year changes broken into component parts
- Source-level contributions to a total change (positive and negative)
- Factor decomposition analysis (Kaya identity, LMDI decomposition)
- Budget or revenue change attribution

## When to Use
- Explaining *why* a total metric changed between two time periods
- Showing which sources drove demand/supply/emission changes
- Decomposing economic, environmental, or energy metrics into contributing factors
- Answering "what drove the increase/decrease?" for policymakers
- Comparing relative contributions of different drivers

## When NOT to Use
> [!warning] Avoid When
> - You only need to show the total change (use a simple bar or waterfall instead)
> - The drivers are not additive to the total (use a different decomposition method)
> - There are too many drivers (>10) making the chart cluttered
> - The time period is continuous rather than point-to-point (use a stacked area instead)

## Real-World Use Cases
- Corporate revenue bridge (product A contributed +$2M, product B contributed -$500K)
- GDP growth decomposition by sector (agriculture, manufacturing, services)
- Population change attribution (births, deaths, migration)
- Cost change drivers in manufacturing

### Energy & Climate Applications
- **Ember's "Change between years" view**: Showing that solar added +200 TWh while coal dropped -150 TWh between 2023 and 2024
- **IEA emission decomposition**: Breaking down CO2 change into energy intensity, carbon intensity, GDP growth, and population growth (Kaya identity)
- **Demand growth attribution**: What drove electricity demand increase — heatwaves, EVs, data centres, heat pumps, economic growth
- **Clean power gap**: How much of demand growth was met by clean sources vs fossil — the "gap" between new clean supply and new demand
- **Country-level generation change**: For India, decomposing +120 TWh into solar (+45), wind (+20), coal (+30), gas (+10), hydro (+15)

## Visual Style Variations
- **Horizontal diverging bar** — positive contributions right, negative left (Ember's approach)
- **Vertical waterfall** — cumulative bridge from start to end value with driver segments
- **Stacked positive/negative bars** — all positive drivers stacked above zero, negative below
- **Butterfly layout** — two sides showing increases vs decreases symmetrically
- **Annotated bar with net line** — individual driver bars with a running net total line

## Related Charts
- [[Waterfall Chart]] — similar bridge concept but for sequential cumulative changes
- [[Tornado Chart]] — similar diverging layout but for sensitivity/scenario analysis
- [[Stacked Bar Chart]] — shows composition but not specifically the change decomposition
- [[Bar Chart]] — simpler comparison without the attribution framing

## Tools That Support This
- Flourish (Ember's choice)
- Datawrapper
- D3.js (custom)
- Tableau (calculated fields)

## Inspiration Sources
- [Ember Electricity Data Explorer — Change between years tab](https://ember-energy.org/data/electricity-data-explorer/) — the canonical implementation
- [IEA — Tracking Clean Energy Progress](https://www.iea.org/topics/tracking-clean-energy-progress) — emission decomposition charts
- [Our World in Data — CO2 Emissions Decomposition](https://ourworldindata.org/co2-emissions) — Kaya identity attribution
