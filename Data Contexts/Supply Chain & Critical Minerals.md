---
title: Supply Chain & Critical Minerals
tags:
  - data-context
  - theme/supply-chain
  - theme/critical-minerals
  - theme/geopolitics
---

# Supply Chain & Critical Minerals

## Overview
Critical minerals data covers the extraction, processing, refining, and manufacturing of materials essential to the energy transition -- lithium, cobalt, nickel, rare earth elements, copper, silicon, graphite, and manganese. This domain tracks geographic concentration risks, price volatility, demand-supply projections, recycling rates, and the geopolitical dynamics shaping mineral security. With clean energy technologies requiring 2-6x more minerals than fossil alternatives, this has become one of the most strategically important data domains.

## Key Data Types
- **Volumetric** — Mine production (tonnes), refining capacity, reserves, resources by country
- **Time series** — Commodity prices ($/tonne), demand forecasts, production growth rates
- **Geographic** — Mining locations, processing hubs, refining concentration by country (HHI scores)
- **Categorical** — Mineral type, end-use application (EV batteries, solar PV, wind turbines, grid), supply chain stage
- **Risk / index** — Supply concentration index, ESG risk in mining, recycling rates, substitution potential

## Key Metrics & Indicators
- **Reserves by country** — Known economically extractable reserves (tonnes) for lithium, cobalt, nickel, copper, REEs
- **Mine production** — Annual output (tonnes) by country and company for each critical mineral
- **Processing/refining share** — Percentage of global processing capacity by country (China dominance metric)
- **Price indices** — Lithium carbonate ($/tonne), cobalt ($/lb), nickel ($/tonne), copper ($/tonne), NdPr oxide ($/kg)
- **Demand forecasts** — Projected mineral demand under IEA NZE, STEPS, and APS scenarios (2030, 2040, 2050)
- **Supply concentration (HHI)** — Herfindahl-Hirschman Index measuring geographic concentration risk
- **Recycling rates** — End-of-life recycling input rate for each mineral (%)
- **Lead times** — Average years from discovery to first production for new mining projects

## Primary Data Sources
- **IEA Critical Minerals** — The Role of Critical Minerals in Clean Energy Transitions, annual market review
- **USGS Mineral Commodity Summaries** — Annual production, reserves, trade data for 90+ mineral commodities
- **British Geological Survey (BGS)** — World Mineral Production, risk list, criticality assessments
- **S&P Global Market Intelligence** — Mine-level production data, cost curves, project pipeline database
- **Benchmark Mineral Intelligence** — Lithium, cobalt, nickel, graphite, rare earth price assessments and forecasts
- **CRU Group** — Commodity analysis for base metals, battery materials, and specialty minerals
- **European Commission Critical Raw Materials Act** — EU criticality assessment, strategic minerals list
- **BloombergNEF** — Battery metals supply tracker, mining and processing capacity databases

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — Lithium carbonate or cobalt price trajectories over 5-10 years with event annotations
- [[Area Chart]] — Projected mineral demand growth under different IEA scenarios (stacked by end-use)
- [[Stacked Bar Chart]] — Annual mine production evolution by country for a given mineral

### For Comparisons
- [[Grouped Bar Chart]] — Compare top 5 producing countries for lithium, cobalt, nickel, copper, and REEs
- [[Radar Chart]] — Multi-dimensional risk profile for each critical mineral (supply concentration, price volatility, recycling rate, substitution potential)
- [[Dumbbell Chart]] — Price range (12-month low to high) across battery metals
- [[Small Multiples]] — Production share by country for 6-8 minerals side by side

### For Composition & Breakdown
- [[Treemap]] — Global lithium or cobalt production by country, with company-level nesting
- [[Stacked Bar Chart]] — End-use demand breakdown by application (EVs, grid storage, consumer electronics, industrial)
- [[Donut Chart]] — Processing concentration for a single mineral (e.g., 70% China for cobalt refining)
- [[Waterfall Chart]] — Supply-demand balance showing production, recycling, and inventory change

### For Relationships & Flows
- [[Sankey Diagram]] — Flow from mining country through refining hub to manufacturing end-use and consuming market
- [[Choropleth Map]] — Mine production or reserves by country, coloured by output level
- [[Bubble Chart]] — Minerals by demand growth rate (x), supply concentration HHI (y), market size (bubble size)
- [[Network Graph]] — Supply chain dependencies showing which countries control which stages for each mineral

## Example Visualizations
- **IEA Critical Minerals** demand growth stacked bar chart under NZE scenario by mineral and end-use
- **USGS** global mine production treemap for lithium with country and company breakdown
- **BloombergNEF** battery metals price index line chart with EV sales overlay
- **S&P Global** cost curve for lithium showing marginal producer breakeven and current price line

## Related Contexts
- [[Energy Markets]]
- [[Renewable Energy & Transition]]
- [[COP UNFCCC IEA]]
- [[Financial Markets]]
