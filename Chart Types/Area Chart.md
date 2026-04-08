---
title: Area Chart
aliases:
  - Filled Line Chart
  - Stacked Area Chart
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/continuous
  - data-type/quantitative
  - data-type/compositional
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - audience/executive
  - theme/energy-markets
  - theme/climate
  - theme/renewable-energy
  - theme/finance
  - theme/iea
  - theme/net-zero
category: Temporal
complexity: intermediate
best_audience: analysts, policymakers, executives
---

# Area Chart

## What It Is
An area chart is a line chart with the region between the line and the axis filled with color or shading. This fill emphasizes the magnitude of values over time rather than just the trend. When multiple series are stacked, the total height represents the aggregate, and each colored band shows a category's contribution to that total. It is one of the most effective chart types for showing both composition and volume simultaneously.

## Best Data Types
- Time series data where cumulative magnitude matters
- Multiple categories contributing to a total over time (stacked variant)
- Continuous quantitative data where the area under the curve is meaningful
- Proportional breakdowns over time (100% stacked variant)

## When to Use
- Showing how a total quantity and its composition change over time
- Emphasizing the volume or cumulative magnitude of a trend (not just direction)
- Visualizing part-to-whole relationships that evolve across a time axis
- Comparing relative contributions of categories to a growing or shrinking total

## When NOT to Use
> [!warning] Avoid When
> - Individual series trends matter more than the aggregate — overlapping areas obscure individual lines, use a [[Line Chart]] instead
> - Categories have similar values causing bands to be indistinguishable — consider small multiples or a [[Stream Graph]]
> - You only have one series and the fill adds no information — a plain [[Line Chart]] is cleaner
> - Precise comparison between categories at a single time point is needed — a [[Stacked Bar Chart]] is easier to read
> - The data has negative values — stacked areas handle negatives poorly

## Real-World Use Cases
- Market share evolution across companies over quarters
- Government revenue composition by tax type over fiscal years
- Population age group distribution over decades
- Website traffic by channel (organic, paid, social, direct) over months

### Energy & Climate Applications
- **Global Energy Generation by Source**: Stacked area showing coal, gas, nuclear, hydro, wind, solar, and other renewables from 1990 to present — the signature IEA/EMBER visualization
- **Cumulative CO2 Emissions by Region**: Historical cumulative emissions stacked by North America, Europe, China, India, rest of Asia, Africa, and others — central to climate equity debates
- **Renewable Investment Trends by Technology**: Annual investment in solar, wind, storage, hydrogen, and other clean energy technologies stacked to show total clean energy investment growth
- **Electricity Generation Mix Projections**: IEA or IRENA scenario projections showing how the generation mix shifts under different policy assumptions through 2050
- **Climate Finance Mobilization**: Annual climate finance stacked by source (public domestic, public international, private) showing growth toward the $100 billion and subsequent goals

## Visual Style Variations
- **Simple area**: single series with filled area below, emphasizing volume
- **Stacked area**: multiple series stacked on top of each other showing total and composition
- **100% stacked area**: each time point normalized to 100%, showing proportional composition changes (total height is constant)
- **Gradient fill**: a single area with gradient from opaque at the line to transparent at the axis, adding depth without heavy color blocks

## Related Charts
- [[Line Chart]] — the unfilled version, better when individual trend comparison matters more than magnitude
- [[Stacked Bar Chart]] — discrete time intervals with easier value reading per category, but less fluid than area
- [[Stream Graph]] — a symmetric, centered variant of the stacked area that emphasizes organic flow and relative changes

## Inspiration Sources
- [EMBER Global Electricity Review](https://ember-climate.org/insights/research/global-electricity-review-2024/) — stacked area charts of electricity generation by source
- [Our World in Data Energy](https://ourworldindata.org/energy) — interactive stacked area charts for global and country energy mixes
- [IEA World Energy Outlook](https://www.iea.org/reports/world-energy-outlook-2023) — scenario-based stacked area projections for energy supply and demand
- [Climate Policy Initiative Landscape of Climate Finance](https://www.climatepolicyinitiative.org/) — annual climate finance flows in stacked area format
- [Global Carbon Project](https://www.globalcarbonproject.org/) — cumulative and annual CO2 emissions by region
