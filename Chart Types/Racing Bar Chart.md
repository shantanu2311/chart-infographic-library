---
title: Racing Bar Chart
aliases:
  - Bar Chart Race
  - Animated Bar Chart
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/ranking
  - data-type/categorical
  - complexity/intermediate
  - audience/general-public
  - audience/executive
  - audience/media
  - theme/energy
  - theme/climate
  - theme/carbon-markets
  - theme/renewable-energy
category: Temporal
complexity: intermediate
best_audience: general public, media, executives
---

# Racing Bar Chart

## What It Is
A racing bar chart is an animated horizontal bar chart that shows how rankings and values change over time. As the animation plays through each time period, bars dynamically grow, shrink, and reorder, creating a compelling visual narrative of competition and change. The format went viral in 2019-2020 and remains one of the most engaging ways to present longitudinal ranking data for broad audiences.

## Best Data Types
- Ranked entities (countries, companies, products) measured over many time periods
- Cumulative metrics that grow over time
- Time series with 10+ time steps and 5-20 competing entities
- Any data where the ranking story matters as much as the values

## When to Use
- Showing how rankings shift over decades (e.g., top emitting countries 1990-2025)
- Presenting cumulative growth races (installed capacity, EV sales, investment)
- Creating engaging social media or presentation content from time-series data
- When the narrative of overtaking and falling behind is the key insight
- Conference presentations where animation captures audience attention

## When NOT to Use
> [!warning] Avoid When
> - Precise value comparison at a specific point in time is needed (use static [[Bar Chart]])
> - The data has fewer than 5 time periods (not enough motion to justify animation)
> - Print or static media where animation cannot play
> - Analytical audiences who need to study the data at their own pace
> - Rankings barely change over time (the animation will be boring)

## Real-World Use Cases
- Most populated countries race from 1950 to present
- Top YouTube channels by subscriber count over time
- GDP by country animated over decades
- Billboard #1 songs cumulative weeks at top

### Energy & Climate Applications
- Top 10 CO2-emitting countries from 1990 to 2025, showing China overtaking the US
- Renewable energy capacity by country race (cumulative GW installed)
- Carbon price evolution across global ETS markets (EU, China, Korea, California)
- Cumulative EV sales by manufacturer showing Tesla, BYD, and others competing
- MDB climate finance commitments by institution over the last decade

## Visual Style Variations
- **Standard race** — horizontal bars with smooth transitions and year counter
- **Cumulative race** — values only grow, showing total accumulated amounts
- **Grouped race** — bars color-coded by region or category within the race
- **Narrated race** — annotations appear at key moments (policy changes, milestones)

## Related Charts
- [[Bump Chart]] — static ranking chart showing position changes over time without animation
- [[Bar Chart]] — static snapshot; the building block of the racing bar chart
- [[Line Chart]] — alternative for showing value trajectories without ranking emphasis

## Tools That Support This
- **Flourish** — most popular no-code bar chart race builder with smooth animations
- **D3.js** — full customization for developers
- **Observable** — notebook-based bar chart race with shareable embeds

## Inspiration Sources
- [Flourish Bar Chart Race Template](https://flourish.studio/visualisations/bar-chart-race/) — drag-and-drop race builder
- [Observable Bar Chart Race](https://observablehq.com/@d3/bar-chart-race) — D3-based implementation with code
