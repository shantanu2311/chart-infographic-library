---
title: Slope Chart
aliases:
  - Slopegraph
  - Before-After Chart
tags:
  - chart-type/specialized
  - data-type/paired-comparison
  - data-type/quantitative
  - data-type/temporal
  - complexity/intermediate
  - audience/executive
  - audience/analyst
  - audience/policymaker
  - audience/general-public
  - theme/climate
  - theme/energy-markets
  - theme/renewable-energy
  - theme/carbon-markets
  - theme/mdb
  - theme/net-zero
category: Specialized
complexity: intermediate
best_audience: executives, analysts, policymakers, general public
---

# Slope Chart

## What It Is
A slope chart compares values for multiple entities at exactly two points in time (or two conditions), with a line connecting each entity's paired values. The slope (angle and direction) of each line immediately communicates whether the entity increased or decreased, and by how much relative to others. Popularized by Edward Tufte, slope charts are remarkably effective at communicating change when the story is a simple before-and-after comparison.

## Best Data Types
- Paired measurements at two discrete time points (before/after, year A vs. year B)
- Pre-intervention vs. post-intervention comparisons across multiple entities
- Two-condition comparisons (e.g., baseline vs. scenario, domestic vs. international)
- Ranked or value data for up to ~15 entities at two points

## When to Use
- Comparing performance, rank, or value changes between exactly two time points
- Highlighting which entities improved most, declined most, or stayed flat
- Telling a clean before/after story (e.g., pre-policy vs. post-policy)
- Replacing a grouped bar chart when the "change" story is more important than the absolute values

## When NOT to Use
> [!warning] Avoid When
> - You have more than two time points — use a [[Line Chart]] or [[Bump Chart]]
> - There are too many entities (more than ~15) and lines overlap heavily — consider filtering or using a [[Dot Plot]]
> - The two time points are not comparable (different methodologies, scopes, or units)
> - Absolute values matter more than direction of change — a [[Bar Chart]] side by side is clearer
> - The data has extreme outliers that compress all other slopes into a flat band

## Real-World Use Cases
- Country life expectancy comparison between 2000 and 2020
- Company market share before and after a merger
- Test scores pre-training and post-training for a cohort
- Crime rates before and after a policy intervention across cities

### Energy & Climate Applications
- **Pre/Post-Paris Agreement Emission Trajectories by Country**: Comparing national emission levels (or emission intensity) in 2015 vs. 2025, showing which countries bent the curve after the Paris Agreement
- **LCOE Changes 2015 vs. 2025 by Technology**: Solar PV, onshore wind, offshore wind, battery storage, gas, coal, and nuclear costs at two points, dramatically showing the cost crossover
- **Carbon Price Shifts Before/After Policy Changes**: EUA prices before and after the Market Stability Reserve introduction, or regional carbon prices before and after linking agreements
- **MDB Climate Finance Allocation Shifts**: Share of MDB lending going to climate projects in 2018 vs. 2023, showing which banks increased their climate share most
- **Renewable Share of Electricity by Country**: Comparing renewable percentage in national electricity mixes at two benchmark years (e.g., 2015 vs. 2025) to show transition leaders and laggards

## Visual Style Variations
- **Classic Tufte style**: minimalist, with labels at both ends of each line and no grid or axis decoration
- **Color-coded direction**: lines colored green for increase, red for decrease, grey for minimal change
- **Highlighted subset**: one or two key entities in bold color, rest in light grey for context
- **Rank-based**: vertical positions show rank rather than value, creating a bump chart with two columns

## Related Charts
- [[Dumbbell Chart]] — shows the same before/after comparison horizontally with dots connected by a bar, often preferred when values cluster closely
- [[Bump Chart]] — extends the slope chart concept to multiple time periods, showing rank evolution
- [[Line Chart]] — the general-purpose multi-period alternative when more than two time points exist

## Inspiration Sources
- [Edward Tufte's "The Visual Display of Quantitative Information"](https://www.edwardtufte.com/tufte/books_vdqi) — the foundational text where slopegraphs were formalized
- [Climate Action Tracker Country Comparisons](https://climateactiontracker.org/) — emission trajectory data for before/after Paris comparisons
- [IRENA Renewable Power Generation Costs](https://www.irena.org/Publications) — LCOE data at multiple snapshots enabling slope chart pairs
- [World Bank Climate Finance Data](https://www.worldbank.org/en/results/2023/11/01/climate-finance) — MDB climate finance share data at different reporting years
- [EMBER Data Explorer](https://ember-climate.org/data/) — country-level renewable share data across years for paired comparisons
