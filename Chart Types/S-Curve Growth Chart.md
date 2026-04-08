---
title: S-Curve Growth Chart
aliases:
  - Exponential Growth Chart
  - Technology Adoption Curve
  - Doubling Time Chart
  - Logistic Growth Chart
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/exponential
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - theme/renewable-energy
  - theme/energy-markets
  - theme/climate
  - theme/net-zero
category: Temporal
complexity: intermediate
best_audience: analysts, policymakers, energy strategists, technology forecasters
---

# S-Curve Growth Chart

## What It Is
A line chart specifically designed to show exponential or logistic (S-shaped) growth trajectories of technologies, markets, or adoption curves. Unlike a standard line chart, the S-curve framing emphasizes the phase of growth — slow start, rapid exponential middle, and eventual plateau. Ember uses this extensively to show solar's explosive trajectory: 100 TWh to 1,000 TWh in just 8 years, then to 2,000 TWh in only 3 more years.

## Best Data Types
- Time series showing exponential or near-exponential growth
- Technology deployment data (cumulative capacity, generation, sales)
- Market penetration rates (% adoption over time)
- Cost decline curves (learning rates)
- Cumulative production or deployment data

## When to Use
- Showing that a technology is on an exponential trajectory (and may be underestimated by linear thinking)
- Comparing growth phases of different technologies (solar vs wind vs EVs)
- Illustrating "doubling time" — how long it takes to double from each milestone
- Making the case for continued acceleration (or predicting saturation)
- Communicating inflection points where growth shifts from slow to rapid

## When NOT to Use
> [!warning] Avoid When
> - The data is genuinely linear — don't force an S-curve narrative on linear growth
> - The technology hasn't yet shown clear exponential signals
> - You need to compare absolute values rather than growth trajectories
> - The audience needs precise short-term forecasts (S-curves are better for long-term framing)
> - Saturation point is highly uncertain — avoid implying a definitive plateau

## Real-World Use Cases
- Technology adoption curves (mobile phones, internet, social media)
- Product lifecycle stages (introduction, growth, maturity, decline)
- Epidemic/pandemic growth curves
- Market penetration of innovations (diffusion of innovations theory)

### Energy & Climate Applications
- **Ember's solar S-curve**: Solar generation from 100 TWh (2016) → 1,000 TWh (2024) → projected 2,000 TWh (2027) — each doubling faster than the last
- **EV adoption curves**: Global EV sales following classic S-curve, with different countries at different phases (Norway near plateau, India in early exponential)
- **Battery cost decline**: $/kWh falling on a learning curve — each doubling of cumulative production reduces cost by ~18%
- **Wind capacity growth**: Tracking cumulative GW additions showing acceleration phases by region
- **Heat pump deployment**: Europe's heat pump adoption curve accelerating post-2022 energy crisis
- **Green hydrogen electrolyzer capacity**: Early exponential phase, useful for projecting when costs cross competitiveness thresholds

## Visual Style Variations
- **Log-scale Y-axis** — makes exponential growth appear as a straight line, revealing the constant growth rate
- **Doubling time annotations** — marking each doubling milestone (100→200→400→800→1,600 TWh) with time intervals
- **Multi-technology overlay** — comparing S-curves of solar, wind, EVs, heat pumps on the same timeline (offset to align by phase)
- **Phase shading** — background bands marking "introduction", "growth", "maturity" phases
- **Projected continuation** — dashed line extending the curve forward with uncertainty band

## Related Charts
- [[Line Chart]] — standard trend display; S-curve adds exponential framing
- [[Area Chart]] — can show cumulative growth with magnitude emphasis
- [[Connected Scatter Plot]] — can show trajectory with two variables simultaneously
- [[Bump Chart]] — shows ranking shifts that often accompany S-curve growth

## Tools That Support This
- D3.js (custom logistic curve fitting)
- Flourish (Ember's tool of choice)
- Python matplotlib/seaborn with scipy curve fitting
- Observable Plot

## Inspiration Sources
- [Ember — Five Charts on the Energy Transition](https://ember-energy.org/latest-insights/marking-five-years-of-ember-with-five-charts-on-the-global-energy-transition/) — solar S-curve "doubling time" chart
- [Our World in Data — Technology Adoption](https://ourworldindata.org/technology-adoption) — classic S-curves across technologies
- [BloombergNEF — New Energy Outlook](https://about.bnef.com/new-energy-outlook/) — energy technology S-curve projections
