---
title: Financial Markets
tags:
  - data-context
  - theme/finance
  - theme/esg
  - theme/green-bonds
---

# Financial Markets

## Overview
Financial markets data in the climate context covers ESG-integrated investing, green and sustainability-linked bonds, climate-aligned equity indices, sovereign credit risk from climate exposure, and carbon futures trading. This domain sits at the intersection of traditional capital markets and climate risk, where physical and transition risks are increasingly priced into asset valuations, credit ratings, and portfolio construction.

## Key Data Types
- **Time series** — Asset prices, index levels, fund flows, issuance volumes (daily, monthly, quarterly)
- **Categorical** — Asset class, instrument type (bond/equity/derivative), ESG rating tier, sector classification
- **Risk metrics** — Climate Value-at-Risk (VaR), transition risk scores, physical risk exposure
- **Ratio / derived** — Greenium (green bond premium), tracking error, Sharpe ratio, portfolio carbon footprint
- **Threshold / binary** — Taxonomy alignment (EU/ASEAN/China), Paris-aligned benchmark eligibility

## Key Metrics & Indicators
- **Green bond issuance** — Annual volume ($bn), cumulative outstanding, by currency and issuer type
- **ESG fund AUM** — Assets under management in ESG-labelled strategies ($tn), net fund flows
- **Climate Value-at-Risk (VaR)** — Potential portfolio loss under warming scenarios (NGFS)
- **Stranded asset exposure** — Value of fossil fuel reserves at risk of non-extraction ($tn)
- **Carbon footprint (WACI)** — Weighted Average Carbon Intensity of portfolio (tCO2e/$M revenue)
- **Greenium** — Yield spread between green bonds and conventional equivalents (basis points)
- **Sovereign climate risk scores** — Country-level ratings integrating physical + transition risk
- **Paris-aligned benchmark tracking** — Number and AUM of EU PAB and CTB indices

## Primary Data Sources
- **Bloomberg Terminal / Bloomberg NEF** — Green bond indices, ESG scores, energy transition investment tracker
- **MSCI** — ESG ratings, climate indices (ACWI Climate Paris Aligned), implied temperature rise
- **S&P Global Sustainable1** — Trucost carbon data, physical risk analytics, EU taxonomy alignment
- **Climate Bonds Initiative (CBI)** — Green bond market intelligence, taxonomy, post-issuance reporting
- **NGFS (Network for Greening the Financial System)** — Climate scenarios for central banks and supervisors
- **Morningstar / Sustainalytics** — ESG risk ratings, fund-level sustainability scores, controversy flags
- **GFANZ (Glasgow Financial Alliance for Net Zero)** — Member commitments, transition plan frameworks
- **PRI (Principles for Responsible Investment)** — Signatory data, reporting frameworks, stewardship activity

## Recommended Chart Types

### For Trends & Time Series
- [[Line Chart]] — Green bond cumulative issuance growth or ESG fund AUM trajectory over years
- [[Candlestick Chart]] — Daily EUA futures or carbon credit price OHLC
- [[Area Chart]] — Quarterly ESG fund net inflows/outflows with cumulative overlay

### For Comparisons
- [[Grouped Bar Chart]] — Green bond issuance by region or currency in a given year
- [[Bullet Chart]] — Fund ESG score vs benchmark ESG score
- [[Dumbbell Chart]] — Greenium spread across sovereign, corporate, and municipal green bonds
- [[Radar Chart]] — Multi-dimensional ESG profile comparison across portfolio holdings

### For Composition & Breakdown
- [[Treemap]] — Green bond market by issuer type (sovereign, corporate, municipal, supranational)
- [[Stacked Bar Chart]] — Use-of-proceeds breakdown for green bond issuance (energy, transport, buildings, water)
- [[Donut Chart]] — Portfolio allocation by EU taxonomy alignment status
- [[Waterfall Chart]] — Attribution of portfolio carbon intensity change (divestment, engagement, rebalancing)

### For Relationships & Flows
- [[Bubble Chart]] — Companies plotted by market cap (x), carbon intensity (y), ESG score (bubble size)
- [[Scatter Plot]] — ESG score vs financial return for equity universe
- [[Heatmap]] — Correlation matrix of ESG factors vs financial performance metrics
- [[Sankey Diagram]] — Capital flow from investor type through instrument to use-of-proceeds category

## Example Visualizations
- **Climate Bonds Initiative** annual State of the Market report green bond issuance bar chart by use of proceeds
- **MSCI** implied temperature rise distribution across global equity index constituents (histogram)
- **NGFS** scenario comparison of GDP impact under orderly vs disorderly transition (line chart with confidence bands)
- **BloombergNEF** annual energy transition investment bar chart reaching $1.8tn milestone

## Related Contexts
- [[Public Finance & MDBs]]
- [[Carbon Markets]]
- [[Energy Markets]]
- [[ESG & Sustainable Finance]]
