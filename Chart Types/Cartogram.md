---
title: Cartogram
aliases:
  - Distorted Map
  - Area Cartogram
  - Value-by-Area Map
tags:
  - chart-type/geospatial
  - data-type/quantitative
  - data-type/ratio
  - complexity/advanced
  - audience/analysts
  - audience/researchers
  - audience/policymakers
  - theme/climate
  - theme/energy
  - theme/finance
  - theme/geopolitics
category: Geospatial
complexity: advanced
best_audience: analysts, researchers, policymakers
---

# Cartogram

## What It Is
A cartogram is a map in which geographic regions are resized proportionally to a data variable rather than their actual land area, while attempting to preserve relative spatial position and adjacency. This technique directly addresses the fundamental flaw of [[Choropleth Map|choropleths]] where visually dominant large-area regions (Russia, Canada, Australia) can distort perception of global patterns. Cartograms force the viewer to confront the data magnitude itself rather than geographic accident.

## Best Data Types
- Absolute totals that benefit from area encoding (e.g., total CO2 emissions by country)
- Population or economic weight measures
- Financial flows and investment volumes
- Cumulative quantities where proportional representation matters
- Any metric where geographic area creates misleading visual weight in standard maps

## When to Use
- Showing each country or region at a size proportional to its contribution (emissions, population, GDP)
- Correcting the visual bias of large but sparsely populated regions in climate or energy data
- Highlighting disproportionate shares in global totals (e.g., top 10 emitters dominating the visual)
- Communicating fairness or equity arguments where per-capita or absolute contribution matters
- Making editorial or advocacy visualizations that provoke reconsideration of standard map perspectives

## When NOT to Use
> [!warning] Avoid When
> - Readers need to identify specific countries by shape; heavy distortion destroys recognizability
> - The data is a rate or ratio rather than an absolute total (use a [[Choropleth Map]] instead)
> - Precise geographic location matters for the analysis
> - The audience is unfamiliar with the technique; cartograms require a moment of orientation that can confuse general audiences
> - You have very few regions (under 10), where a [[Treemap]] or ranked bar chart communicates more clearly

## Real-World Use Cases
- World population cartogram where India and China dominate the visual field
- Electoral cartograms resizing constituencies by voter count rather than land area
- Global GDP cartogram showing economic weight of nations
- Scientific publication output cartogram by country

### Energy & Climate Applications
- Countries sized by annual CO2 emissions, making China, the US, and India visually dominant while shrinking geographically large but low-emitting nations
- Population-weighted carbon footprint cartogram revealing per-capita inequities between Global North and South
- MDB climate finance lending volume distorted map, resizing recipient countries by World Bank or ADB disbursement amounts
- Renewable installed capacity cartogram showing where wind and solar GW are actually concentrated globally
- Cumulative historical emissions cartogram for equity arguments in UNFCCC loss-and-damage negotiations

## Visual Style Variations
- **Contiguous cartogram** (Gastner-Newman diffusion) preserving topology with smooth distortion of boundaries
- **Non-contiguous cartogram** where regions shrink or grow as separate shapes with gaps between them
- **Dorling cartogram** replacing regions with uniform circles sized by value, arranged to approximate geographic position
- **Rectangular/tile cartogram** using equal-sized tiles in a grid layout that loosely mirrors geography (common for US state maps)

## Related Charts
- [[Choropleth Map]] — standard geographic coloring without area distortion; better for rates and ratios
- [[Bubble Map]] — overlays sized circles on an undistorted base map as a less radical alternative
- [[Treemap]] — hierarchical area-based visualization without any geographic constraint
- [[Waffle Chart]] — grid-based proportional display that can serve similar equity-communication goals

## Inspiration Sources
- [Worldmapper](https://worldmapper.org/) — extensive gallery of global cartograms on hundreds of topics including energy and emissions
- [Max Roser / Our World in Data](https://ourworldindata.org/) — occasional use of population-scaled cartograms for emissions equity arguments
- [Washington Post — Election Cartograms](https://www.washingtonpost.com/graphics/) — high-quality Dorling and tile cartograms for political data
- [go-cart.io](https://go-cart.io/) — open-source Gastner-Newman cartogram generator for custom datasets
