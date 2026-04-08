---
title: Bump Chart
aliases:
  - Ranking Chart
  - Rank Chart
chart_type: bump-chart
category: temporal
data_types:
  - time-series
  - categorical
data_contexts:
  - Renewable Energy & Transition
  - Carbon Markets
  - Energy Markets
complexity: medium
audience:
  - media
  - technical
  - policymaker
visual_styles:
  - editorial
  - data-journalism
  - minimal
color_approach: categorical
libraries:
  - d3
  - plotly
  - flourish
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/temporal
  - data-type/ordinal
  - data-type/ranking
  - data-type/time-series
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/policymaker
  - theme/energy-markets
  - theme/renewable-energy
  - theme/carbon-markets
  - theme/climate
  - theme/net-zero
---

# Bump Chart

## What It Is
A bump chart shows how the rankings of multiple entities change over time. Each entity is represented by a line connecting its rank positions across time periods, with the vertical axis showing rank (typically 1 at the top) and the horizontal axis showing time. Crossings between lines immediately reveal when one entity overtakes another. By encoding rank rather than raw values, bump charts eliminate scale differences and focus attention purely on relative position changes.

## Best Data Types
- Rankings or ordinal positions tracked across discrete time periods
- Competitive standings where relative position matters more than absolute values
- League table or index data with periodic updates
- Any data where "who is ahead" matters more than "by how much"

## When to Use
- Showing which countries, companies, or technologies are rising or falling in rank over time
- Communicating competitive dynamics and overtaking moments
- Simplifying multi-line charts by converting values to ranks (eliminates the spaghetti problem)
- Highlighting dramatic rank changes or persistent leaders/laggards

## When NOT to Use
> [!warning] Avoid When
> - Absolute values or magnitudes matter — a [[Line Chart]] preserves this information
> - You have more than ~15 entities — even with ranks, too many crossing lines create visual noise
> - There is only one time period — a simple ordered [[Bar Chart]] shows a single ranking more clearly
> - Ties are frequent — bump charts handle ties poorly since lines must share a rank position
> - The audience needs to understand the gap between ranks — bump charts show order but not distance

## Real-World Use Cases
- Formula 1 driver standings across a season
- University rankings across annual publications
- Billboard chart positions of songs over weeks
- Brand perception rankings across quarterly surveys

### Energy & Climate Applications
- **Country Rankings by Renewable Share**: How nations rank by percentage of electricity from renewables across years — showing Nordic countries consistently high while others rapidly climb
- **Carbon Market Exchange Rankings by Volume**: ICE, EEX, KRX, and other exchanges ranked by carbon trading volume across quarters, showing market consolidation or fragmentation
- **Top Emitting Sector Ranking Shifts**: Ranking of power, industry, transport, buildings, agriculture, and waste sectors by emission volume over decades as decarbonization reshapes the order
- **Technology Cost Competitiveness Rankings**: Solar PV, onshore wind, offshore wind, gas CCGT, nuclear, and coal ranked by LCOE over years, showing the dramatic rise of renewables
- **Climate Performance Index Country Rankings**: Germanwatch CPI or similar index rankings showing which countries improve or decline in climate policy performance across assessment years

## Visual Style Variations
- **Connected dots**: dots at each time point connected by lines, the classic bump chart form
- **Thick colored lines**: each entity gets a distinct thick line with label at the endpoint
- **Highlighted trajectory**: one or two entities highlighted in color with all others in grey
- **Annotated crossings**: key overtaking moments annotated with text or markers

## Related Charts
- [[Slope Chart]] — a bump chart with only two time periods, showing a single before-after rank comparison
- [[Line Chart]] — shows absolute values over time rather than ranks; use when magnitude matters
- [[Alluvial Diagram]] — shows categorical migration over stages with proportional band widths, a richer but more complex alternative

## Inspiration Sources
- [Germanwatch Climate Change Performance Index](https://www.germanwatch.org/en/CCPI) — annual country climate performance rankings
- [REN21 Renewables Global Status Report](https://www.ren21.net/gsr/) — country renewable energy share rankings over years
- [BloombergNEF LCOE Data](https://about.bnef.com/) — technology cost rankings enabling LCOE bump charts
- [Ember Country Comparisons](https://ember-climate.org/data/data-tools/data-explorer/) — electricity generation share rankings by country
