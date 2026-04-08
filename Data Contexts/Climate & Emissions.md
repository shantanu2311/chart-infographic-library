---
title: Climate & Emissions
tags:
  - data-context
  - theme/climate
  - theme/emissions
  - theme/ghg
---

# Climate & Emissions

## Overview
Climate and emissions data tracks the physical science of global warming alongside anthropogenic greenhouse gas inventories at global, national, sectoral, and facility levels. This domain bridges atmospheric measurements (CO2 concentrations, temperature anomalies) with policy-relevant accounting (NDCs, carbon budgets, emission trajectories). It is foundational to nearly every other data context in climate intelligence.

## Key Data Types
- **Time series** — Annual/monthly GHG emissions, atmospheric concentrations, temperature records
- **Categorical** — Gas type (CO2, CH4, N2O, F-gases), sector (energy, IPPU, AFOLU, waste), scope (1/2/3)
- **Geographic** — Country-level inventories, grid-cell climate data, regional emission maps
- **Scenario / projection** — IPCC pathways (SSP1-5), IEA scenarios, NDC conditional/unconditional targets
- **Intensity / normalised** — Emissions per capita, per GDP, per unit output, per MWh

## Key Metrics & Indicators
- **Atmospheric CO2 concentration** — Parts per million (ppm), Mauna Loa / NOAA
- **Global mean temperature anomaly** — Degrees C above pre-industrial (1850-1900 baseline)
- **Annual global GHG emissions** — GtCO2e (all gases) and GtCO2 (fossil CO2 only)
- **Emission intensity** — tCO2e per capita, tCO2e per $1M GDP (PPP)
- **Carbon budget remaining** — GtCO2 remaining for 1.5C and 2C pathways (from IPCC AR6)
- **NDC ambition gap** — Difference between pledged reductions and pathway-consistent targets
- **Methane emissions** — MtCH4 from fossil fuels, agriculture, and waste (UNEP Global Methane Assessment)
- **Land use sink/source balance** — GtCO2 net from LULUCF sector

## Primary Data Sources
- **UNFCCC National Inventory Submissions** — Official country GHG inventories reported under the Paris Agreement
- **IPCC Assessment Reports (AR6, SR1.5)** — Physical science basis, mitigation pathways, carbon budgets
- **Global Carbon Project (GCP)** — Annual Global Carbon Budget with fossil + land use CO2 estimates
- **Climate Action Tracker (CAT)** — Independent scientific analysis of NDCs, policies, and warming projections
- **WRI Climate Watch (CAIT)** — Historical emissions data explorer by country, sector, and gas
- **NOAA / NASA GISS** — Atmospheric CO2 measurements and global temperature records
- **EDGAR (JRC)** — Emissions Database for Global Atmospheric Research, gridded and country-level
- **Our World in Data** — Curated, open-access visualisations of emissions, energy, and climate data

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — Global CO2 emissions trajectory from 1750 to present, or temperature anomaly time series
- [[Area Chart]] — Stacked global emissions by gas type (CO2, CH4, N2O, F-gases) showing composition over time
- [[Sparkline]] — Compact country-level emission trend indicators in a comparison table

### For Comparisons
- [[Grouped Bar Chart]] — Compare top-20 emitting countries in a single year
- [[Stacked Bar Chart]] — NDC target vs current policy trajectory vs 1.5C pathway for key countries
- [[Slope Chart]] — Shift in emission rankings between two time periods (e.g., 2000 vs 2023)
- [[Lollipop Chart]] — Emission intensity (tCO2e/capita) ranked across 30+ countries

### For Composition & Breakdown
- [[Waterfall Chart]] — Decompose year-on-year emission change by sector (energy, transport, industry, buildings, AFOLU)
- [[Treemap]] — Global emissions breakdown by country nested within region
- [[Donut Chart]] — Share of global emissions by gas type or by scope (1/2/3) for a corporate inventory
- [[Stacked Area Chart]] — Sectoral emission shares evolving over decades

### For Relationships & Flows
- [[Choropleth Map]] — Per-capita emissions or emission intensity by country
- [[Scatter Plot]] — GDP per capita vs emissions per capita (Kaya identity decomposition)
- [[Sankey Diagram]] — Flow from primary energy source through sector to GHG gas output
- [[Bubble Chart]] — Countries plotted by GDP (x), emissions (y), population (bubble size)

## Example Visualizations
- **Global Carbon Project** annual budget figure showing fossil CO2 sources and sinks (stacked area)
- **Climate Action Tracker** warming projection thermometer with NDC ranges and current policy bands
- **Our World in Data** per-capita CO2 emissions choropleth map with time slider
- **IPCC AR6 WG3** sectoral emission waterfall showing mitigation potential by measure

## Related Contexts
- [[Net Zero Pathways]]
- [[Carbon Markets]]
- [[COP UNFCCC IEA]]
- [[ESG & Sustainable Finance]]
