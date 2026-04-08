---
title: Connected Scatter Plot
aliases:
  - Connected Dot Plot
  - Trajectory Plot
chart_type: connected-scatter-plot
category: relationship
data_types:
  - continuous
  - time-series
  - paired
data_contexts:
  - Climate & Emissions
  - Renewable Energy & Transition
complexity: medium
audience:
  - technical
  - media
  - academic
visual_styles:
  - editorial
  - data-journalism
color_approach: sequential
libraries:
  - d3
  - plotly
  - datawrapper
  - matplotlib
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/relationship
  - data-type/bivariate
  - data-type/time-series
  - data-type/trajectory
  - complexity/intermediate
  - audience/analyst
  - audience/researcher
  - audience/policymaker
  - theme/energy
  - theme/climate
  - theme/finance
  - theme/net-zero
  - theme/carbon-markets
---

# Connected Scatter Plot

## What It Is
A connected scatter plot is a scatter plot where sequential data points are joined by lines, revealing the trajectory or path that a relationship takes over time. Unlike a standard [[Scatter Plot]] which shows static correlation, the connecting lines add a temporal dimension, showing how the x-y relationship evolves. This creates a visual narrative of progress, regression, or cyclical movement through a two-variable space.

## Best Data Types
- Two continuous variables measured at sequential time points
- Trajectories showing how a relationship evolves (e.g., GDP vs. emissions over decades)
- Path data where order matters (temporal, spatial, or process sequence)
- Paired time series where the x-y relationship shifts over time

## When to Use
- Showing how two related metrics co-evolve over time (decoupling narratives)
- Visualizing whether a country or entity is improving on both dimensions simultaneously
- Tracing the path of investment returns vs. risk over multiple periods
- When the shape of the trajectory (loops, reversals, acceleration) is the insight
- Comparing trajectories of multiple entities through the same x-y space

## When NOT to Use
> [!warning] Avoid When
> - Time is better shown on an explicit axis (use [[Line Chart]] with dual y-axes)
> - The path crosses itself many times, creating visual confusion
> - You have too many entities (more than 5-6 trajectories overlap badly)
> - The temporal ordering of points is not meaningful
> - Precise time-to-value lookup is needed (connecting lines obscure chronology)

## Real-World Use Cases
- Hans Rosling's Gapminder: GDP per capita vs. life expectancy trajectories by country
- Phillips Curve: unemployment vs. inflation path over economic cycles
- Product lifecycle: price vs. market share trajectory
- Sports analytics: offensive vs. defensive performance season-by-season

### Energy & Climate Applications
- GDP vs. CO2 emissions trajectory over decades (showing decoupling when path bends right-and-down)
- Renewable investment volume vs. deployment rate evolution by country
- Carbon price vs. ETS coverage progression showing market maturity paths
- Energy intensity vs. GDP per capita trajectory for developing economies
- R&D spending vs. patent filings in clean energy technology over time

## Visual Style Variations
- **Labeled points** — year or period labels on each dot for chronological reference
- **Arrow-headed** — directional arrows on connecting lines showing time flow
- **Multi-entity** — several trajectories in different colors overlaid on same axes
- **Gradient path** — line color shifts from light to dark encoding time progression

## Related Charts
- [[Scatter Plot]] — static version without temporal connection; shows correlation not trajectory
- [[Line Chart]] — shows each variable against time separately; loses x-y relationship
- [[Slope Chart]] — compares two time points for multiple entities; simpler but only two snapshots

## Tools That Support This
- **D3.js** — full control over path rendering and annotations
- **Datawrapper** — connected scatter plot chart type with labeled points
- **ggplot2** — `geom_path()` in R for publication-quality trajectory plots

## Inspiration Sources
- [Datawrapper Connected Scatter](https://www.datawrapper.de/charts/scatter-plot) — examples and design guidance
- [Gapminder](https://www.gapminder.org/tools/) — the canonical GDP vs. life expectancy connected scatter
