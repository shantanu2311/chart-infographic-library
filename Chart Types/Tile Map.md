---
title: Tile Map
aliases:
  - Grid Map
  - Hex Tile Map
  - Cartogram Grid
chart_type: tile-map
category: spatial
data_types:
  - geographic
  - categorical
  - continuous
data_contexts:
  - Climate & Emissions
  - Carbon Markets
  - Renewable Energy & Transition
complexity: medium
audience:
  - media
  - policymaker
  - public
visual_styles:
  - editorial
  - data-journalism
  - minimal
color_approach: sequential
libraries:
  - d3
  - flourish
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/geospatial
  - data-type/geographic
  - data-type/categorical
  - data-type/quantitative
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - audience/general-public
  - theme/energy
  - theme/climate
  - theme/renewable-energy
  - theme/carbon-markets
  - theme/net-zero
---

# Tile Map

## What It Is
A tile map replaces the irregular geographic shapes of a traditional [[Choropleth Map]] with equal-sized tiles — squares, hexagons, or other uniform shapes — arranged to approximate the spatial relationships between regions. This eliminates the geographic size bias that plagues choropleths (where large, sparsely populated regions dominate visually) and ensures every region, regardless of physical area, receives equal visual weight. Each tile is then colored or labeled to encode data.

## Best Data Types
- One value per geographic region (state, country, district)
- Categorical data mapped to regions (policy status: yes/no/pending)
- Quantitative data where equal visual weight per region matters
- Binary or ordinal classifications across geographic units

## When to Use
- Comparing Indian states where Rajasthan's area would otherwise dominate a choropleth
- Showing policy adoption status across US states or EU member states with equal weight
- When the per-region story matters more than geographic accuracy
- Avoiding the visual bias where geographically large but data-small regions dominate
- Presenting results of state-level or country-level surveys and indices

## When NOT to Use
> [!warning] Avoid When
> - Geographic proximity and spatial patterns are the primary insight (use [[Choropleth Map]])
> - The audience expects a true geographic map and may be confused by tile arrangement
> - Continuous spatial data needs interpolation (use heatmaps or contour maps)
> - You have too many regions (100+ tiles become hard to arrange and label)
> - The data varies by sub-regional boundaries that tiles cannot represent

## Real-World Use Cases
- US election results by state using equal-sized hexagons
- NPR and FiveThirtyEight state-level policy tracker tiles
- EU member state comparison dashboards eliminating France/Germany size dominance
- Australian state/territory equal-tile maps

### Energy & Climate Applications
- Indian state comparison of renewable energy installed capacity (28 states as equal tiles)
- US state carbon pricing or RPS (Renewable Portfolio Standard) adoption status
- EU member state ETS auction revenue per capita, each country as one hex
- Equal-area country grid showing NDC target ambition level (traffic light coloring)
- Indian state-wise grid emission factors with equal visual weight per state

## Visual Style Variations
- **Square grid** — uniform squares in rough geographic arrangement
- **Hexagonal grid** — hexagons for tighter packing and organic feel
- **Labeled tiles** — state/country abbreviations inside each tile
- **Choropleth tiles** — color gradient on tiles encoding continuous values

## Related Charts
- [[Choropleth Map]] — traditional geographic map; better for spatial patterns, worse for equal weighting
- [[Cartogram]] — distorts actual geography by area to encode values; retains shape hints
- [[Heatmap]] — grid-based value display; similar visual but not geographic

## Tools That Support This
- **Flourish** — built-in tile map (hex and square) with Indian and US templates
- **D3.js** — custom tile grid layout with flexible tile shapes
- **Datawrapper** — hex tile maps for US states and other geographies

## Inspiration Sources
- [Flourish Tile Map Templates](https://flourish.studio/visualisations/maps/) — ready-made tile maps for multiple geographies
- [Datawrapper Hex Map Guide](https://blog.datawrapper.de/hex-tile-maps/) — design principles for tile maps vs. choropleths
