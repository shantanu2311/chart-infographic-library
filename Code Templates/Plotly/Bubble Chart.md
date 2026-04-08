---
title: Bubble Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: bubble-chart
library: plotly
---

# Bubble Chart — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Bubble Chart — Plotly Starter
# Data format: DataFrame with x, y, size, and optional color columns

df = pd.DataFrame({
    "Production": [120, 85, 200, 150, 60, 180, 95],
    "Emissions": [8.2, 4.5, 12.5, 9.8, 3.2, 11.0, 6.3],
    "Energy_GJ": [500, 200, 800, 350, 150, 600, 280],
    "Plant": ["Plant A", "Plant B", "Plant C", "Plant D", "Plant E", "Plant F", "Plant G"],
    "Process": ["EAF", "Induction", "EAF", "Re-rolling", "Induction", "EAF", "Re-rolling"],
})

fig = px.scatter(
    df,
    x="Production",
    y="Emissions",
    size="Energy_GJ",
    color="Process",
    hover_name="Plant",
    size_max=50,
    color_discrete_map={"EAF": "#e63946", "Induction": "#457b9d", "Re-rolling": "#2a9d8f"},
    title="Production vs Emissions (bubble size = energy consumption)",
    labels={
        "Production": "Production (tonnes/month)",
        "Emissions": "Emissions (tCO2e)",
        "Energy_GJ": "Energy (GJ)",
    },
)

fig.update_traces(marker=dict(line=dict(width=1, color="white"), opacity=0.8))

fig.update_layout(
    height=500,
    plot_bgcolor="white",
)

fig.update_xaxes(showgrid=True, gridcolor="#f0f0f0")
fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `size` — column for bubble sizing (area-proportional by default)
- `size_max` — maximum bubble diameter in pixels
- `hover_name` — column shown as bold title in hover tooltip
- `hover_data` — dict of extra columns and format strings for tooltip

## Energy/Climate Data Example
```python
# Steel plants: production vs emissions, bubble = energy use
df = pd.DataFrame({
    "Production": [120, 85, 200, 150, 60],
    "Emissions": [8.2, 4.5, 12.5, 9.8, 3.2],
    "Energy_GJ": [500, 200, 800, 350, 150],
    "Plant": ["EAF-1", "IF-1", "EAF-2", "RR-1", "IF-2"],
    "Process": ["EAF", "Induction", "EAF", "Re-rolling", "Induction"],
})
```

## Customization Tips
- Add `trendline="ols"` for a regression line through the bubble centers
- Use `animation_frame="Year"` for animated bubble chart over time (Gapminder-style)
- Add `marginal_x="histogram"` for distribution context on the x-axis
- Use `fig.add_shape(type="circle", ...)` for reference bubble in legend

## Related
- [[Bubble Chart]] — chart type reference
- [[Bubble Chart — D3 Template]] — D3.js alternative
