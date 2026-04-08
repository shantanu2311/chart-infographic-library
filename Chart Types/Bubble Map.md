---
title: Bubble Map
aliases:
  - Proportional Symbol Map
  - Graduated Symbol Map
  - Point Map
chart_type: bubble-map
category: spatial
data_types:
  - geographic
  - continuous
  - categorical
data_contexts:
  - Renewable Energy & Transition
  - Energy Markets
  - Supply Chain & Critical Minerals
  - Ember Global Electricity Data
complexity: medium
audience:
  - executive
  - policymaker
  - technical
visual_styles:
  - editorial
  - corporate
  - data-journalism
color_approach: categorical
libraries:
  - d3
  - plotly
  - echarts
  - flourish
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/geospatial
  - data-type/quantitative
  - data-type/point-location
  - data-type/multi-variable
  - complexity/intermediate
  - audience/analysts
  - audience/policymakers
  - audience/investors
  - theme/energy
  - theme/climate
  - theme/supply-chain
  - theme/critical-minerals
  - theme/infrastructure
---

# Bubble Map

## What It Is
A bubble map places proportionally sized circles at geographic coordinates to represent quantitative values tied to specific locations or aggregated regions. Unlike a [[Choropleth Map]] that fills entire administrative boundaries with color, bubble maps preserve the base geography while overlaying data as a distinct visual layer. This makes them well suited for point-level data such as facility locations, project sites, or city-level metrics where the exact position carries meaning.

## Best Data Types
- Point-located quantitative data (e.g., power plant capacity at lat/long coordinates)
- City-level or site-level aggregations on a national or regional base map
- Multi-variable data using bubble size for one dimension and color for another
- Counts or totals at discrete locations (e.g., number of carbon credit projects per site)
- Infrastructure density and spatial distribution patterns

## When to Use
- Showing the location and relative magnitude of facilities, projects, or events on a map
- Comparing point-level values across a geography without distorting regional boundaries
- Encoding two variables simultaneously (size + color) for richer spatial analysis
- Presenting infrastructure or asset portfolios with geographic context
- When data is tied to specific coordinates rather than entire administrative regions

## When NOT to Use
> [!warning] Avoid When
> - Data points are extremely dense and overlapping, making individual bubbles unreadable (consider aggregation or a [[Heatmap]])
> - The data is a regional rate or ratio covering entire administrative boundaries (use a [[Choropleth Map]])
> - Precise value comparison is needed; circle area perception is imprecise, especially across distant map regions
> - You have fewer than 5 data points; a table or annotated map would be simpler
> - Bubble sizes span several orders of magnitude, causing tiny bubbles to become invisible next to large ones

## Real-World Use Cases
- Earthquake maps with circles sized by magnitude at epicenter coordinates
- City population maps showing urban agglomerations as proportional bubbles
- Disease outbreak maps with case counts at reporting locations
- Retail store locations sized by revenue on a national map

### Energy & Climate Applications
- Power plant locations sized by installed capacity (MW), colored by fuel type (coal, gas, solar, wind)
- Carbon credit project sites from Verra or Gold Standard registries, sized by annual emission reductions
- EV charging infrastructure density across a country, with bubble size indicating number of charge points per city
- Renewable energy project pipeline by location, sized by planned capacity and colored by development stage
- Critical mineral mining sites (lithium, cobalt, rare earths) sized by production volume, overlaid on geopolitical boundaries
- IEA or IRENA facility-level data showing clean energy manufacturing plants sized by output capacity

## Visual Style Variations
- **Single-variable bubbles** with size encoding one metric and a uniform color
- **Bivariate bubbles** using size for one variable (e.g., capacity) and color saturation for another (e.g., utilization factor)
- **Categorical color + size** combining fuel-type or technology-type color coding with magnitude sizing
- **Clustered bubbles** that aggregate nearby points into larger composite circles at lower zoom levels, expanding on zoom-in

## Related Charts
- [[Choropleth Map]] — better for region-level rates and ratios where boundaries define the data
- [[Scatter Plot]] — similar size/color encoding but on abstract axes rather than geographic coordinates
- [[Bubble Chart]] — the non-geographic equivalent using x/y axes with sized and colored points
- [[Cartogram]] — alternative approach that distorts the map itself rather than overlaying symbols
- [[Heatmap]] — continuous density surface alternative when points are too numerous for individual bubbles

## Inspiration Sources
- [Global Energy Monitor](https://globalenergymonitor.org/projects/global-coal-plant-tracker/tracker/) — interactive bubble maps of coal, gas, solar, and wind plants worldwide
- [Carbon Brief — Mapped: The world's coal power plants](https://www.carbonbrief.org/) — power station bubble maps with capacity sizing
- [Resource Watch (WRI)](https://resourcewatch.org/) — multi-layer bubble maps combining energy, climate, and environmental datasets
- [Mapbox Examples](https://docs.mapbox.com/mapbox-gl-js/example/) — technical reference for building performant web-based bubble maps
