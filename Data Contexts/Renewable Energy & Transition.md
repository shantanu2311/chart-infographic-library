---
title: Renewable Energy & Transition
tags:
  - data-context
  - theme/renewable-energy
  - theme/energy-transition
  - theme/clean-tech
---

# Renewable Energy & Transition

## Overview
Renewable energy and energy transition data tracks the deployment, economics, and grid integration of solar, wind, hydro, geothermal, and emerging clean technologies worldwide. This domain covers installed capacity, generation output, levelised costs, investment flows, auction results, and grid-level integration challenges including curtailment, storage, and flexibility. It is one of the fastest-moving data domains, with cost curves and deployment figures updating materially each year.

## Key Data Types
- **Time series** — Annual installed capacity, generation, investment, LCOE (yearly and quarterly)
- **Categorical** — Technology type (solar PV, onshore wind, offshore wind, CSP, hydro, geothermal, biomass), market segment (utility, C&I, residential)
- **Geographic** — Country/region deployment, resource quality maps (solar irradiance, wind speed)
- **Economic** — LCOE, LCOS, auction prices, PPA prices, capex/opex per MW, subsidy levels
- **Performance** — Capacity factor, curtailment rates, grid penetration share, storage duration

## Key Metrics & Indicators
- **Installed capacity** — GW of solar, wind, hydro, and other renewables by country and globally
- **Electricity generation** — TWh produced by technology, share of total generation mix
- **LCOE (Levelised Cost of Energy)** — $/MWh for utility-scale solar, onshore/offshore wind, battery storage
- **Annual investment** — $bn deployed in clean energy by technology, region, and financing type
- **Capacity factor** — Actual generation as % of theoretical maximum (technology and location dependent)
- **Auction/PPA prices** — Contracted prices for new renewable capacity ($/MWh)
- **Grid penetration** — Renewables share of total electricity supply (%)
- **Battery storage deployment** — GW and GWh of grid-scale and behind-the-meter storage installed

## Primary Data Sources
- **IRENA (International Renewable Energy Agency)** — Renewable Capacity Statistics, Renewable Power Generation Costs, REmap
- **IEA** — Renewables Market Report, World Energy Outlook renewables chapters, PVPS/Wind TCP
- **BloombergNEF** — New Energy Outlook, LCOE benchmarks, clean energy investment tracker
- **REN21** — Renewables Global Status Report, policy database, renewable share tracker
- **Ember** — Global Electricity Review, monthly generation data, coal-to-clean tracker
- **SolarPower Europe / WindEurope / GWEC** — Technology-specific deployment data and outlooks
- **Lazard** — Levelised Cost of Energy and Levelised Cost of Storage annual analyses
- **BNEF / Wood Mackenzie** — Auction databases, PPA price trackers, project-level data

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — LCOE decline curves for solar PV, onshore wind, offshore wind, and batteries (2010-2025)
- [[Area Chart]] — Stacked global electricity generation mix showing renewables growth crowding out coal
- [[Stacked Bar Chart]] — Annual clean energy investment by technology (solar, wind, EVs, storage, hydrogen)

### For Comparisons
- [[Grouped Bar Chart]] — Installed capacity additions by country (China, US, India, EU) in a single year
- [[Dumbbell Chart]] — LCOE range (min-max) for each renewable technology vs fossil fuel comparators
- [[Slope Chart]] — Shift in technology cost rankings between 2015 and 2025
- [[Small Multiples]] — Capacity factor distributions across geographies for solar and wind

### For Composition & Breakdown
- [[Stacked Area Chart]] — Evolution of global power generation mix by source over 30 years
- [[Treemap]] — Global installed solar capacity by country, sized proportionally
- [[Donut Chart]] — Share of annual investment by technology category
- [[Waterfall Chart]] — Decompose year-on-year generation growth by technology (solar added, wind added, coal retired)

### For Relationships & Flows
- [[Scatter Plot]] — Country-level solar irradiance (x) vs installed capacity per capita (y) showing deployment efficiency
- [[Bubble Chart]] — Countries by GDP (x), renewable share (y), total capacity (bubble size)
- [[Sankey Diagram]] — Flow from investment through technology deployment to generation output and emission reduction
- [[Heatmap]] — Monthly capacity factors by region and technology (12 months x N regions)

## Example Visualizations
- **IRENA Renewable Power Generation Costs** LCOE decline line chart with learning rate annotations
- **BloombergNEF** annual global energy transition investment bar chart surpassing $1 trillion
- **Ember Global Electricity Review** stacked area of generation mix with solar/wind inflection point
- **Lazard LCOE** technology comparison waterfall showing unsubsidised cost ranges vs marginal fossil costs

## Related Contexts
- [[Energy Markets]]
- [[Net Zero Pathways]]
- [[Supply Chain & Critical Minerals]]
- [[Climate & Emissions]]
