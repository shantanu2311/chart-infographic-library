---
title: Candlestick Chart
aliases:
  - OHLC Chart
  - Japanese Candlestick Chart
  - K-Line Chart
tags:
  - chart-type/temporal
  - data-type/financial
  - data-type/ohlc
  - data-type/time-series
  - complexity/intermediate
  - audience/analyst
  - audience/trader
  - audience/finance-professional
  - theme/energy-markets
  - theme/finance
  - theme/carbon-markets
  - theme/critical-minerals
  - theme/renewable-energy
category: Temporal
complexity: intermediate
best_audience: analysts, traders, finance professionals
---

# Candlestick Chart

## What It Is
A candlestick chart displays four data points per time interval — open, high, low, and close (OHLC) — using a rectangular body and vertical wicks. The body spans from open to close price, colored to indicate direction (typically green/hollow for up, red/filled for down). The wicks extend to the high and low values. Originating in 18th-century Japanese rice trading, candlestick charts remain the standard for financial market analysis because they pack maximum price information into a compact, pattern-rich format.

## Best Data Types
- Financial OHLC price data at regular intervals (minute, hourly, daily, weekly)
- Any metric with open/close/high/low semantics per period
- Commodity spot and futures prices
- Market trading data where intra-period volatility and direction both matter

## When to Use
- Analyzing price movements in traded commodities, allowances, or financial instruments
- Identifying technical patterns (doji, hammer, engulfing) for market analysis
- Showing both trend direction and intra-period volatility simultaneously
- Presenting market data to an audience familiar with financial charting conventions

## When NOT to Use
> [!warning] Avoid When
> - The data lacks OHLC structure — a [[Line Chart]] is appropriate for single-value time series
> - The audience is non-financial and unfamiliar with candlestick conventions — use a simpler [[Line Chart]]
> - You want to show long-term trends spanning decades — aggregation loses the candle pattern detail, switch to a [[Line Chart]]
> - The data has very low volatility making candles appear as flat lines — a [[Line Chart]] is more informative
> - You need to compare multiple instruments simultaneously — overlapping candlesticks are unreadable

## Real-World Use Cases
- Equity market daily trading analysis (S&P 500, individual stocks)
- Forex pair analysis (EUR/USD, GBP/USD) at various timeframes
- Cryptocurrency market analysis (BTC/ETH daily candles)
- Agricultural commodity futures (wheat, corn, soybeans)

### Energy & Climate Applications
- **EU ETS Carbon Allowance (EUA) Prices**: Daily or weekly candles for EUA futures on ICE or EEX, the most liquid carbon market instrument, showing the interplay of policy announcements, auction results, and compliance cycles
- **Brent Crude Oil Futures**: The global oil benchmark traded on ICE, where candlestick patterns reflect OPEC decisions, geopolitical events, and demand shifts from energy transition
- **Lithium Carbonate Spot Prices**: Battery-grade lithium prices on the Shanghai Metals Market or Fastmarkets, tracking the critical mineral's volatile pricing that affects EV and storage costs
- **Renewable Energy Certificate (REC) Trading**: I-REC, TIGR, and GO (Guarantee of Origin) certificate prices showing seasonal patterns and policy-driven demand
- **Voluntary Carbon Credit Prices**: Verra VCU and Gold Standard credit prices by vintage and project type, revealing market sentiment and quality premiums

## Visual Style Variations
- **Traditional Japanese**: green (or hollow) for bullish candles, red (or filled) for bearish candles
- **Hollow candles**: body is outlined (hollow) when close is above open, filled when below — with color encoding close vs. prior close
- **OHLC bars**: the open-high-low-close data rendered as horizontal ticks on a vertical line instead of candle bodies
- **Volume underlay**: candlesticks overlaid on a volume bar chart to correlate price moves with trading activity
- **Heikin-Ashi**: modified candles using averaged values to smooth trends and reduce noise

## Related Charts
- [[Line Chart]] — uses only closing prices, losing OHLC detail but cleaner for long-term trend views and non-financial audiences
- [[Bar Chart]] — for non-financial categorical comparisons; OHLC bars are a financial-specific bar variant
- [[Box Plot]] — shares the whisker-and-body visual language but summarizes distributions rather than time-series OHLC data

## Inspiration Sources
- [ICE Endex EUA Futures](https://www.ice.com/products/197/EUA-Futures) — live EU carbon allowance candlestick charting
- [Trading Economics Commodities](https://tradingeconomics.com/commodities) — Brent crude, natural gas, and energy commodity candlestick data
- [Shanghai Metals Market](https://www.metal.com/) — lithium and battery metal spot price candles
- [S&P Global Platts Carbon Trading](https://www.spglobal.com/commodityinsights/en) — carbon and energy price analytics
- [TradingView](https://www.tradingview.com/) — interactive candlestick charting for energy commodities and carbon markets
