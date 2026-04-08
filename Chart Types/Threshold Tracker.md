---
title: Threshold Tracker
aliases:
  - Milestone Tracker Chart
  - Threshold Crossing Chart
  - Adoption Threshold Chart
  - Phase-Down Tracker
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/categorical
  - complexity/intermediate
  - audience/policymaker
  - audience/analyst
  - theme/climate
  - theme/renewable-energy
  - theme/coal-phase-down
  - theme/net-zero
category: Temporal
complexity: intermediate
best_audience: policymakers, advocates, energy analysts
---

# Threshold Tracker

## What It Is
A visualization tracking how many entities (countries, companies, facilities, etc.) have crossed a defined threshold over time. Rather than showing the raw metric for each entity, it aggregates: "In 2015, 59 countries were above 20% coal; by 2024, only 40 were." This creates a powerful narrative of collective progress (or regression) toward a milestone. Ember uses this to track coal phase-down across countries.

## Best Data Types
- Count of entities exceeding/falling below a threshold over time
- Binary state tracking (above/below target) aggregated across a population
- Milestone achievement rates across countries, companies, or facilities
- Compliance or target attainment tracking

## When to Use
- Tracking collective progress toward a threshold (e.g., % of countries with >50% renewables)
- Showing phase-down of a harmful technology (countries exiting coal)
- Monitoring policy adoption rates (how many jurisdictions have carbon pricing)
- Communicating momentum: "the number of countries that have crossed X is accelerating"
- Simplifying complex multi-country data into a single compelling trend

## When NOT to Use
> [!warning] Avoid When
> - The threshold is arbitrary and misleading (cherry-picking a number to fit narrative)
> - Individual entity trajectories matter more than the aggregate count
> - The population of entities is changing over time (new countries forming, companies merging)
> - Continuous metric values are more informative than binary above/below

## Real-World Use Cases
- Countries achieving universal literacy or vaccination targets over decades
- Companies adopting net-zero targets (Net Zero Tracker)
- Cities achieving air quality standards
- Schools meeting educational benchmarks

### Energy & Climate Applications
- **Ember's coal phase-down tracker**: Countries with coal share >20% declining from 59 (2015) to 40 (2024)
- **Renewable milestone tracker**: Countries where solar+wind exceed 20% of generation — count rising each year
- **Net-zero target tracker**: Countries with legislated net-zero targets increasing from 2 (2015) to 80+ (2025)
- **Carbon pricing adoption**: Jurisdictions with carbon pricing rising from 20 (2010) to 70+ (2024)
- **EU coal exit tracker**: EU countries with coal below 5% — 19 out of 27 in 2025
- **NDC ambition ladder**: Countries with "1.5C-compatible" NDCs vs "insufficient" — tracking shifts after each COP

## Visual Style Variations
- **Step line chart** — y-axis is count of entities above/below threshold, stepping up/down at each change point
- **Stacked area** — entities above threshold (one color) vs below (another), showing the shift
- **Animated map** — countries lighting up or fading as they cross the threshold
- **Small multiples** with threshold line — individual entity charts with a horizontal reference line, ordered by when they crossed
- **Progress bar / gauge** — "X out of Y countries have achieved the target"

## Related Charts
- [[Line Chart]] — for the individual entity trends underlying the threshold
- [[Choropleth Map]] — shows geographic distribution of above/below threshold at a point in time
- [[Bump Chart]] — shows ranking changes that may correlate with threshold crossings
- [[Gauge Chart]] — single-point "X of Y achieved" display
- [[Small Multiples]] — individual entity views with threshold reference line

## Tools That Support This
- Flourish (Ember's choice)
- D3.js (custom)
- Observable Plot
- Datawrapper

## Inspiration Sources
- [Ember — Coal generation in OECD](https://ember-energy.org/latest-insights/coal-generation-in-oecd-countries-falls-below-half-of-its-peak/) — coal phase-down threshold tracking
- [Net Zero Tracker](https://zerotracker.net/) — tracking net-zero commitments across countries and companies
- [World Bank Carbon Pricing Dashboard](https://carbonpricingdashboard.worldbank.org/) — jurisdictions with carbon pricing over time
