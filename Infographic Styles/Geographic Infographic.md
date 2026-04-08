---
title: Geographic Infographic
tags:
  - infographic-style
  - maps
  - geospatial
  - climate-vulnerability
  - critical-minerals
  - emissions-mapping
---

# Geographic Infographic

## What It Is
A map-centric infographic format that uses geographic representations as the primary visual scaffold to display spatial patterns, regional variations, and jurisdictional data. It leverages the reader's spatial intuition to reveal distribution patterns, concentration hotspots, and geographic disparities that tables and charts cannot convey. This format is essential when location is a meaningful variable in the data story.

## Key Characteristics
- Map as the dominant visual element occupying 50-70% of the layout
- Color-encoded regions (choropleth) or sized markers (proportional symbols) for data encoding
- Legend with clear breakpoints and units
- Inset panels or callout boxes for regional deep-dives or small territories
- Supplementary charts alongside the map providing non-spatial context

## Best Use Cases
- Global CO2 emissions by country with per-capita overlays
- Renewable energy resource potential maps (solar irradiance, wind speed, geothermal)
- Carbon pricing jurisdiction map showing ETS, carbon tax, and hybrid schemes worldwide
- Critical mineral deposit locations (lithium, cobalt, rare earths) mapped against supply chain concentration
- Climate vulnerability indices showing physical risk exposure across regions
- Energy access gaps and electrification rates across sub-Saharan Africa and South Asia

### Energy & Climate Applications
- Global emissions cartogram where country size reflects total GHG output rather than land area
- India grid region emission factor map showing regional variation (NE=0.476 vs N=0.898 tCO2e/MWh)
- EU CBAM coverage map showing affected trade corridors and exposed exporter countries
- Renewable energy auction results by Indian state with capacity awarded in GW
- Climate adaptation funding flows from donor countries to vulnerable regions via MDB channels

## Structure & Layout
The map occupies the central canvas. A title and subtitle sit above, establishing the variable being mapped and the time period. The legend is positioned in a consistent corner (typically bottom-left or top-right) with no more than 5-7 color classes for choropleth maps. Callout lines connect specific regions to annotation boxes containing statistics or narrative context. Below or beside the map, 2-3 supporting charts (bar, small multiples, or sparklines) provide additional dimensions that cannot be encoded spatially. For global maps, an equal-area projection (Robinson or Equal Earth) is preferred over Mercator to avoid distorting the Global South.

## Design Tips
> [!tip] Best Practices
> - Use sequential color scales (light to dark) for magnitude data and diverging scales (blue-white-red) for data with a meaningful midpoint
> - Always use an equal-area projection for thematic maps — Mercator distorts Africa and South Asia, exactly the regions most relevant to climate analysis
> - Include inset maps for small but important territories (Singapore, small island states, city-states)
> - Label only the top 5-10 regions to avoid clutter; let the color encoding carry the remaining information
> - Add a "no data" category in the legend and color it neutral grey — missing data is itself informative

## When NOT to Use
> [!warning] Avoid When
> - Geography is not a meaningful variable in the data (using a map just because you have country names wastes space)
> - You are comparing only 2-3 specific countries in detail (use a comparison infographic instead)
> - The data varies more by sector or time than by location

## Recommended Chart Types
- [[Choropleth Map]] — color-encoded regions for continuous variables like emissions intensity or renewable share
- [[Bubble Map]] — proportional circles placed on geographic coordinates for discrete facilities or projects
- [[Cartogram]] — distorted geography where region size encodes the data variable (e.g., emissions-weighted world map)

## Inspiration Sources
- [Our World in Data CO2 Explorer](https://ourworldindata.org/co2-emissions) — interactive global emissions choropleth
- [World Bank Carbon Pricing Dashboard](https://carbonpricingdashboard.worldbank.org/) — jurisdiction-level carbon pricing map
- [Global Solar Atlas](https://globalsolaratlas.info/) — solar resource potential mapping with high spatial resolution
