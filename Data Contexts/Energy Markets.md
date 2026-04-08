---
title: Energy Markets
tags:
  - data-context
  - theme/energy-markets
  - theme/commodities
  - theme/trading
---

# Energy Markets

## Overview
Energy markets encompass the trading, pricing, and physical delivery of oil, natural gas, coal, and electricity across spot and futures exchanges worldwide. These markets are shaped by geopolitical events, seasonal demand patterns, infrastructure constraints, and the accelerating energy transition. Data in this domain is high-frequency, volatile, and deeply interconnected across fuel types and geographies.

## Key Data Types
- **Time series** — Price histories (intraday, daily, weekly, monthly, annual) for spot and futures contracts
- **Categorical** — Fuel type, grade, delivery hub, contract expiry, market segment
- **Geographic** — Production basins, pipeline routes, LNG shipping lanes, grid regions
- **Volumetric** — Production, consumption, trade flows, storage levels (barrels, BCM, TWh, tonnes)
- **Ratio / derived** — Crack spreads, spark spreads, dark spreads, capacity utilisation, stock-to-use ratios

## Key Metrics & Indicators
- **Brent Crude (ICE)** — Global oil benchmark, $/barrel
- **WTI Crude (NYMEX)** — US oil benchmark, $/barrel
- **Henry Hub Natural Gas** — US gas benchmark, $/MMBtu
- **TTF (Title Transfer Facility)** — European gas benchmark, EUR/MWh
- **API2 Coal (ICE)** — Northwest European coal benchmark, $/tonne
- **Wholesale electricity prices** — Day-ahead and real-time by grid zone ($/MWh or EUR/MWh)
- **OPEC+ production quotas and compliance** — Million barrels per day (mb/d)
- **Global oil/gas inventory levels** — US SPR, OECD commercial stocks, EU gas storage fill rates

## Primary Data Sources
- **IEA (International Energy Agency)** — Monthly Oil Market Report, World Energy Outlook, Gas Market Report
- **OPEC Monthly Oil Market Report** — Production data, demand forecasts, spare capacity estimates
- **US EIA (Energy Information Administration)** — Weekly petroleum status, Short-Term Energy Outlook, AEO
- **BloombergNEF** — Energy price indices, transition investment data, LCOE benchmarks
- **S&P Global Commodity Insights (Platts)** — Platts assessments for crude, refined products, gas, LNG, coal, power
- **ICE / CME / NYMEX** — Futures and options data, open interest, settlement prices
- **Ember** — Global electricity generation mix, power sector emissions
- **JODI (Joint Organisations Data Initiative)** — Oil and gas transparency data from producing and consuming nations

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — Track Brent, WTI, Henry Hub, TTF price evolution over months/years
- [[Candlestick Chart]] — Show OHLC (open-high-low-close) for daily/weekly energy futures
- [[Area Chart]] — Visualise cumulative supply or demand trajectories with shaded confidence bands
- [[Sparkline]] — Embed compact price trend indicators in dashboard summary tables

### For Comparisons
- [[Grouped Bar Chart]] — Compare spot prices across fuel types or regional hubs at a point in time
- [[Dumbbell Chart]] — Show price range between contract months (contango/backwardation spread)
- [[Slope Chart]] — Compare year-over-year price shifts across multiple energy commodities
- [[Small Multiples]] — Juxtapose price patterns across 6-8 regional electricity markets

### For Composition & Breakdown
- [[Stacked Area Chart]] — Show global primary energy mix evolution (oil, gas, coal, nuclear, renewables)
- [[Donut Chart]] — OPEC vs non-OPEC production share at a single point in time
- [[Treemap]] — Breakdown of global oil production by country or company
- [[Waterfall Chart]] — Decompose quarter-over-quarter change in oil demand by driver (transport, industry, petchem)

### For Relationships & Flows
- [[Sankey Diagram]] — Map energy flows from primary production through transformation to end use
- [[Scatter Plot]] — Correlate oil price with GDP growth, or gas price with temperature anomaly
- [[Heatmap]] — Show hourly electricity prices across days of the week (time-of-use pattern)
- [[Chord Diagram]] — Visualise bilateral LNG or crude trade flows between exporting and importing regions

## Example Visualizations
- **IEA Oil Market Report** supply-demand balance stacked bar with stock change overlay
- **BloombergNEF** global LCOE trend lines for solar, wind, gas, and coal generation (2010-2025)
- **EIA Weekly Petroleum Status** crude inventory deviation from 5-year range (area chart with band)
- **Ember Global Electricity Review** stacked area of generation mix by source with coal peak annotation

## Related Contexts
- [[Carbon Markets]]
- [[Renewable Energy & Transition]]
- [[Supply Chain & Critical Minerals]]
- [[Financial Markets]]
