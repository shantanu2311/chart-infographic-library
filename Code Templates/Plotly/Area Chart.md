---
title: Area Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: area-chart
library: plotly
---

# Area Chart — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Area Chart — Plotly Starter (Stacked)
# Data format: DataFrame with date column and one column per series

df = pd.DataFrame({
    "Year": [2019, 2020, 2021, 2022, 2023] * 4,
    "Source": (["Coal"] * 5 + ["Gas"] * 5 + ["Solar"] * 5 + ["Wind"] * 5),
    "TWh": [
        1028, 966, 1052, 1098, 1078,   # Coal
        62, 60, 63, 66, 68,             # Gas
        39, 54, 73, 91, 113,            # Solar
        65, 68, 72, 76, 82,             # Wind
    ],
})

fig = px.area(
    df,
    x="Year",
    y="TWh",
    color="Source",
    color_discrete_map={
        "Coal": "#4a4a4a",
        "Gas": "#7eb0d5",
        "Solar": "#f7c948",
        "Wind": "#5ab47a",
    },
    title="India Electricity Generation Mix (TWh)",
)

fig.update_layout(
    height=450,
    plot_bgcolor="white",
    hovermode="x unified",
    legend=dict(orientation="h", y=-0.15),
)

fig.update_xaxes(showgrid=False)
fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `groupnorm` — set to `"percent"` in `px.area()` for 100% stacked area
- `line_shape` — `"spline"` for smooth curves, `"linear"` for straight segments
- `stackgroup` — when using `go.Scatter`, set same group name to stack traces
- `opacity` — layer transparency (default 1.0 for px.area)

## Energy/Climate Data Example
```python
# India electricity generation mix (TWh) by year and source
df = pd.DataFrame({
    "Year": [2019, 2020, 2021, 2022, 2023] * 5,
    "Source": ["Coal"]*5 + ["Gas"]*5 + ["Solar"]*5 + ["Wind"]*5 + ["Hydro"]*5,
    "TWh": [
        1028, 966, 1052, 1098, 1078,
        62, 60, 63, 66, 68,
        39, 54, 73, 91, 113,
        65, 68, 72, 76, 82,
        162, 155, 151, 158, 162,
    ],
})
```

## Customization Tips
- Use `go.Scatter(fill="tonexty", stackgroup="one")` for manual stacking control
- Add `groupnorm="percent"` parameter for proportional (100%) view
- Set `line=dict(width=0)` to remove line borders between areas
- Use `fig.update_traces(hovertemplate=...)` for custom tooltip format

## Related
- [[Area Chart]] — chart type reference
- [[Area Chart — D3 Template]] — D3.js alternative
