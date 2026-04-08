---
title: Scatter Plot — Plotly Template
tags:
  - code-template
  - plotly
chart_type: scatter-plot
library: plotly
---

# Scatter Plot — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Scatter Plot — Plotly Starter
# Data format: DataFrame with x, y, and optional color column

df = pd.DataFrame({
    "Production_tonnes": [120, 85, 200, 150, 60, 180, 95, 110, 250, 70],
    "Emissions_tCO2e": [8.2, 6.1, 12.5, 9.8, 4.3, 11.0, 7.2, 7.9, 15.1, 5.5],
    "Process": ["EAF", "Induction", "EAF", "Re-rolling", "Induction",
                "EAF", "Re-rolling", "Induction", "EAF", "Re-rolling"],
})

fig = px.scatter(
    df,
    x="Production_tonnes",
    y="Emissions_tCO2e",
    color="Process",
    color_discrete_map={"EAF": "#e63946", "Induction": "#457b9d", "Re-rolling": "#2a9d8f"},
    title="Production vs Emissions by Process Type",
    labels={
        "Production_tonnes": "Production (tonnes/month)",
        "Emissions_tCO2e": "Emissions (tCO2e)",
    },
)

fig.update_traces(marker=dict(size=10, line=dict(width=1, color="white")))

fig.update_layout(
    height=450,
    plot_bgcolor="white",
)

fig.update_xaxes(showgrid=True, gridcolor="#f0f0f0")
fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `color` — categorical column for color grouping with automatic legend
- `size` — numeric column for bubble sizing (turns into bubble chart)
- `trendline` — `"ols"` for linear regression, `"lowess"` for smooth fit (needs statsmodels)
- `hover_data` — list of extra columns to show in tooltip

## Energy/Climate Data Example
```python
# Steel plant production vs GHG emissions
df = pd.DataFrame({
    "Production_tonnes": [120, 85, 200, 150, 60],
    "Emissions_tCO2e": [8.2, 6.1, 12.5, 9.8, 4.3],
    "Process": ["EAF", "Induction", "EAF", "Re-rolling", "Induction"],
    "Intensity": [0.068, 0.072, 0.063, 0.065, 0.072],
})
```

## Customization Tips
- Add `trendline="ols"` for a regression line (requires `pip install statsmodels`)
- Use `symbol="Process"` to vary marker shapes by category
- Add `marginal_x="histogram"` and `marginal_y="box"` for distribution context
- Use `fig.add_hline(y=threshold)` to add reference lines

## Related
- [[Scatter Plot]] — chart type reference
- [[Scatter Plot — D3 Template]] — D3.js alternative
