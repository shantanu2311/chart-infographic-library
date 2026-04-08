---
title: Choropleth Map
aliases:
  - Thematic Map
  - Shaded Map
  - Color-coded Map
tags:
  - chart-type/geospatial
  - data-type/categorical
  - data-type/continuous
  - data-type/ratio
  - complexity/intermediate
  - audience/policymakers
  - audience/analysts
  - audience/general-public
  - theme/energy
  - theme/climate
  - theme/geopolitics
category: Geospatial
complexity: intermediate
best_audience: policymakers, analysts, general public
---

# Choropleth Map

## What It Is
A choropleth map colors geographic regions (countries, states, districts) according to a data variable, using a sequential or diverging color scale to encode magnitude. It is one of the most widely recognized forms of geospatial visualization, making it effective for communicating regional patterns to broad audiences. The approach works best when the underlying data is inherently tied to the geographic boundaries being displayed.

## Best Data Types
- Rates, ratios, and percentages (e.g., renewable share of electricity mix)
- Normalized values per capita or per unit area
- Indexed scores and rankings (e.g., climate vulnerability index)
- Categorical classifications with ordered levels (e.g., NDC ambition tiers)
- Census or survey data aggregated to administrative boundaries

## When to Use
- Comparing a single metric across many geographic regions simultaneously
- Revealing spatial clusters, gradients, or outliers in national or sub-national data
- Communicating policy coverage or regulatory status across jurisdictions
- Showing progress toward targets where geography matters (e.g., energy access)
- Presenting data to non-technical audiences who intuitively read maps

## When NOT to Use
> [!warning] Avoid When
> - Regions vary enormously in area, causing large low-density regions to dominate visually (consider a [[Cartogram]] instead)
> - The data is not normalized; raw totals on a choropleth mislead because larger regions appear more significant
> - You need to show point-level data such as individual project sites (use a [[Bubble Map]])
> - The number of regions is very small (fewer than 5), where a bar chart would be clearer
> - Precise value comparison is required; color perception is imprecise across non-adjacent regions

## Real-World Use Cases
- Election result maps showing vote share by constituency
- Public health dashboards mapping disease prevalence by district
- Economic indicators (GDP per capita, unemployment rate) across countries
- Education attainment levels by state or province

### Energy & Climate Applications
- Country-level carbon pricing coverage showing which nations have an ETS, carbon tax, both, or neither
- Renewable energy share of total electricity generation by nation (IEA Global Energy Review style)
- Grid emission factors by region within a country (e.g., India's five grid regions ranging from 0.476 to 0.898 tCO2e/MWh)
- NDC ambition ratings mapped globally (Climate Action Tracker color tiers)
- Energy access rates by country in Sub-Saharan Africa and South Asia
- Climate vulnerability index by nation, combining exposure, sensitivity, and adaptive capacity scores

## Visual Style Variations
- **Sequential palette** for data ranging from low to high (e.g., light yellow to dark red for emission intensity)
- **Diverging palette** centered on a meaningful midpoint (e.g., blue-white-red for above/below average temperature anomaly)
- **Classified (stepped) breaks** using quantiles or natural breaks for cleaner categorical reading
- **Unclassed (continuous) gradient** for smooth transitions that preserve data fidelity

## Related Charts
- [[Cartogram]] — distorts region size by the data variable, solving the area-bias problem of choropleths
- [[Bubble Map]] — overlays proportional symbols on geography for point or aggregated data
- [[Heatmap]] — uses color intensity on a grid rather than geographic boundaries
- [[Bar Chart]] — often a better choice when precise comparison matters more than spatial context

## Inspiration Sources
- [Our World in Data — CO2 Emissions](https://ourworldindata.org/co2-emissions) — exemplary choropleth maps of per-capita emissions and energy mix by country
- [Climate Action Tracker](https://climateactiontracker.org/countries/) — NDC ambition rating map with clear categorical color scheme
- [IEA Data Explorer](https://www.iea.org/data-and-statistics) — interactive choropleths for energy indicators across 190+ countries
- [D3 Observable Choropleth](https://observablehq.com/@d3/choropleth) — canonical implementation reference for web-based choropleths
