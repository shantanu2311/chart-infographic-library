---
title: Choropleth Map — Plotly Template
tags:
  - code-template
  - plotly
chart_type: choropleth-map
library: plotly
---

# Choropleth Map — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Choropleth Map — Plotly Starter
# Data format: DataFrame with location codes and values; GeoJSON for boundaries

# World map example using built-in country codes
df = pd.DataFrame({
    "Country": ["IND", "CHN", "USA", "DEU", "BRA", "JPN", "GBR", "AUS", "ZAF", "RUS"],
    "Emissions_MtCO2": [2900, 11400, 5100, 650, 480, 1060, 330, 400, 470, 1750],
    "Country_Name": ["India", "China", "USA", "Germany", "Brazil",
                     "Japan", "UK", "Australia", "South Africa", "Russia"],
})

fig = px.choropleth(
    df,
    locations="Country",
    locationmode="ISO-3",        # ISO 3166-1 alpha-3 codes
    color="Emissions_MtCO2",
    hover_name="Country_Name",
    color_continuous_scale="YlOrRd",
    title="CO2 Emissions by Country (MtCO2, 2023)",
    labels={"Emissions_MtCO2": "MtCO2"},
)

fig.update_layout(
    height=500,
    geo=dict(
        showframe=False,
        showcoastlines=True,
        coastlinecolor="#ccc",
        projection_type="natural earth",
    ),
    coloraxis_colorbar=dict(title="MtCO2"),
)

fig.show()
```

## Configuration Options
- `locationmode` — `"ISO-3"`, `"USA-states"`, `"country names"`, or use `geojson` parameter
- `projection_type` — `"natural earth"`, `"mercator"`, `"orthographic"`, `"equirectangular"`
- `color_continuous_scale` — `"YlOrRd"`, `"Blues"`, `"Viridis"`, `"Plasma"`
- `geo.scope` — `"world"`, `"usa"`, `"europe"`, `"asia"`, `"africa"`

## Energy/Climate Data Example
```python
# CO2 emissions by country (MtCO2, 2023 estimates)
df = pd.DataFrame({
    "Country": ["IND", "CHN", "USA", "DEU", "BRA", "JPN"],
    "Emissions_MtCO2": [2900, 11400, 5100, 650, 480, 1060],
    "Country_Name": ["India", "China", "USA", "Germany", "Brazil", "Japan"],
})
```

## Customization Tips
- For Indian states, load a GeoJSON file and use `geojson=` parameter with `featureidkey`
- Use `px.choropleth_mapbox()` for interactive tile-based maps (needs Mapbox token or open-street-map)
- Add `animation_frame="Year"` to animate across time periods
- Use `fig.update_geos(fitbounds="locations")` to auto-zoom to data coverage

## Related
- [[Choropleth Map]] — chart type reference
- [[Choropleth Map — D3 Template]] — D3.js alternative
