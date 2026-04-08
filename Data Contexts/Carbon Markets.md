---
title: Carbon Markets
tags:
  - data-context
  - theme/carbon-markets
  - theme/emissions-trading
  - theme/climate-policy
---

# Carbon Markets

## Overview
Carbon markets encompass both compliance systems (cap-and-trade programmes like the EU ETS, China ETS, RGGI, and K-ETS) and voluntary carbon markets (Verra VCS, Gold Standard, ACR, CAR). They also include emerging mechanisms under Article 6 of the Paris Agreement and CORSIA for international aviation. This domain tracks carbon credit/allowance pricing, issuance and retirement volumes, market coverage, and the integrity of offset methodologies.

## Key Data Types
- **Time series** — Allowance/credit prices (daily, weekly), auction clearing prices, trading volumes
- **Categorical** — Market type (compliance/voluntary), credit standard, methodology, project type, vintage year
- **Geographic** — Jurisdiction (national/subnational ETS), project host country, buyer country
- **Volumetric** — Issuances, retirements, cancellations (MtCO2e), free allocation vs auctioned allowances
- **Policy / regulatory** — Cap trajectory, MSR (Market Stability Reserve) thresholds, CBAM phase-in, Article 6 rules

## Key Metrics & Indicators
- **EUA price (EU ETS)** — European Union Allowance price, EUR/tCO2e
- **CCA price (California)** — California Carbon Allowance, $/tCO2e
- **China ETS allowance price** — CNY/tCO2e
- **VCM issuance and retirement volumes** — Annual MtCO2e issued and retired by standard (Verra, GS, ACR)
- **Compliance market coverage** — Percentage of global GHG emissions covered by a carbon pricing mechanism
- **Carbon price per tCO2e** — Across all major compliance and voluntary markets
- **CORSIA eligible credits** — Volume of offsets eligible under the aviation carbon offsetting scheme
- **Article 6.4 credits** — Issuances under the new UN crediting mechanism (successor to CDM)

## Primary Data Sources
- **ICAP (International Carbon Action Partnership)** — ETS map, allowance price tracker, annual status report
- **Ecosystem Marketplace** — State of the Voluntary Carbon Markets, VCM data and insights
- **Refinitiv / LSEG Carbon** — EUA, UKA, CCA price data, carbon market research
- **S&P Global Commodity Insights** — Platts carbon assessments, voluntary credit pricing (Nature-Based, Tech-Based)
- **World Bank Carbon Pricing Dashboard** — Global coverage map, revenue data, price levels across 70+ jurisdictions
- **Verra Registry** — VCS project database, issuance and retirement records
- **Gold Standard Impact Registry** — Project data, credit issuance and retirement, SDG contributions
- **Berkeley Carbon Trading Project** — Voluntary market transaction data and analytics

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — EUA price history from Phase 1 through Phase 4, or VCM annual issuance volumes
- [[Candlestick Chart]] — Daily or weekly EUA/CCA futures OHLC for trading analysis
- [[Area Chart]] — Cumulative VCM issuances vs retirements showing growing credit surplus or deficit

### For Comparisons
- [[Grouped Bar Chart]] — Compare carbon prices across major compliance markets (EU, China, California, Korea, UK)
- [[Heatmap]] — Monthly carbon price levels across 10+ compliance markets (rows) over years (columns)
- [[Slope Chart]] — Year-over-year price shift across compliance and voluntary market benchmarks

### For Composition & Breakdown
- [[Stacked Bar Chart]] — VCM issuance by project type (REDD+, renewables, cookstoves, industrial gas, biochar)
- [[Treemap]] — Global compliance market coverage by jurisdiction, sized by covered emissions
- [[Donut Chart]] — Share of total credits by standard (Verra, Gold Standard, ACR, CAR, Plan Vivo)
- [[Funnel Chart]] — Progression from registered projects to issued credits to retired credits (attrition view)

### For Relationships & Flows
- [[Sankey Diagram]] — Flow of carbon credits from project type through standard to buyer sector/region
- [[Choropleth Map]] — Carbon price levels by country/jurisdiction on a world map
- [[Scatter Plot]] — Credit price vs co-benefit score (SDG contributions) across voluntary projects
- [[Heatmap]] — Correlation between EUA price and natural gas price, coal price, power sector emissions

## Example Visualizations
- **ICAP Annual Status Report** choropleth showing global ETS coverage with price colour coding
- **Ecosystem Marketplace** VCM issuance and retirement stacked bar chart by project category (2010-2025)
- **World Bank Carbon Pricing Dashboard** global map of carbon pricing instruments with price bubble overlay
- **Refinitiv** EUA price line chart with MSR threshold annotations and policy event markers

## Related Contexts
- [[Climate & Emissions]]
- [[Financial Markets]]
- [[COP UNFCCC IEA]]
- [[Energy Markets]]
