---
title: Choropleth Map — D3.js Template
tags:
  - code-template
  - d3
chart_type: choropleth-map
library: d3
---

# Choropleth Map — D3.js

## Setup
```bash
npm install d3 topojson-client
# You also need a GeoJSON/TopoJSON file for your geography
```

## Basic Template
```javascript
// Choropleth Map — D3.js v7 Starter
// Data format: GeoJSON + lookup map { featureId: value }

import * as d3 from "d3";
import * as topojson from "topojson-client";

const width = 800;
const height = 500;

const svg = d3
  .select("#chart")
  .append("svg")
  .attr("viewBox", `0 0 ${width} ${height}`)
  .attr("preserveAspectRatio", "xMidYMid meet");

// Value lookup by feature ID (e.g., state name or ISO code)
const values = {
  Maharashtra: 0.672,
  "Tamil Nadu": 0.617,
  Gujarat: 0.672,
  "Uttar Pradesh": 0.898,
  Karnataka: 0.617,
  "West Bengal": 0.826,
  Rajasthan: 0.672,
  "Madhya Pradesh": 0.672,
  Punjab: 0.898,
  Assam: 0.476,
};

// Color scale
const colorScale = d3.scaleSequential(d3.interpolateYlOrRd)
  .domain([0.4, 1.0]);

// Projection — centered on India
const projection = d3.geoMercator()
  .center([82, 22])
  .scale(900)
  .translate([width / 2, height / 2]);

const path = d3.geoPath().projection(projection);

// Load GeoJSON (replace URL with your actual source)
d3.json("https://raw.githubusercontent.com/geohacker/india/master/state/india_state.geojson")
  .then((geojson) => {
    // Draw states
    svg.selectAll("path")
      .data(geojson.features)
      .join("path")
      .attr("d", path)
      .attr("fill", (d) => {
        const val = values[d.properties.NAME_1];
        return val ? colorScale(val) : "#eee";
      })
      .attr("stroke", "#fff")
      .attr("stroke-width", 0.5);

    // Labels (optional — only for larger states)
    svg.selectAll("text")
      .data(geojson.features)
      .join("text")
      .attr("transform", (d) => `translate(${path.centroid(d)})`)
      .attr("text-anchor", "middle")
      .style("font-size", "8px")
      .style("fill", "#333")
      .text((d) => d.properties.NAME_1);
  });
```

## Configuration Options
- `projection` — try `d3.geoNaturalEarth1()` for world maps, `d3.geoAlbersUsa()` for US
- `scale` — zoom level; adjust with `.center()` to frame the region
- `colorScale` — `d3.scaleQuantize` for binned colors, `d3.scaleThreshold` for custom breaks
- `stroke-width` — border thickness between features

## Energy/Climate Data Example
```javascript
// Grid emission factors by state (tCO2e/MWh)
const values = {
  Maharashtra: 0.672,
  "Tamil Nadu": 0.617,
  "Uttar Pradesh": 0.898,
  "West Bengal": 0.826,
  Karnataka: 0.617,
  Assam: 0.476,
  Punjab: 0.898,
  Gujarat: 0.672,
};
```

## Customization Tips
- Add zoom/pan with `d3.zoom()` for large maps
- Use TopoJSON for smaller file size: `topojson.feature(topo, topo.objects.states)`
- Add a legend bar using a thin SVG rect filled with the gradient
- Implement hover effects: highlight borders and show tooltip with state name + value

## Related
- [[Choropleth Map]] — chart type reference
- [[Choropleth Map — Plotly Template]] — Plotly alternative
