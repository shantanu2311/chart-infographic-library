---
title: Line Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: line-chart
library: plotly
---

# Line Chart — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Line Chart — Plotly Starter
# Data format: lists of x (dates/numbers) and y values

years = [2017, 2018, 2019, 2020, 2021, 2022, 2023, 2024]
grid_ef = [0.92, 0.90, 0.88, 0.85, 0.82, 0.79, 0.76, 0.71]

fig = go.Figure()

fig.add_trace(go.Scatter(
    x=years,
    y=grid_ef,
    mode="lines+markers",
    name="Grid EF",
    line=dict(color="#2563eb", width=2.5),
    marker=dict(size=7),
))

fig.update_layout(
    title="India Grid Emission Factor Trend",
    xaxis_title="Year",
    yaxis_title="tCO2e/MWh",
    height=400,
    plot_bgcolor="white",
    hovermode="x unified",
)

fig.update_xaxes(showgrid=True, gridcolor="#f0f0f0", dtick=1)
fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `mode` — `"lines"`, `"markers"`, `"lines+markers"`, `"lines+markers+text"`
- `line.shape` — `"linear"`, `"spline"`, `"hv"` (step), `"vh"` (step)
- `hovermode` — `"x unified"` for combined tooltip, `"closest"` for nearest point
- `fill` — `"tozeroy"` to fill area under the line

## Energy/Climate Data Example
```python
# India grid emission factor by year (tCO2e/MWh)
years = [2017, 2018, 2019, 2020, 2021, 2022, 2023, 2024]
grid_ef = [0.92, 0.90, 0.88, 0.85, 0.82, 0.79, 0.76, 0.71]
target = [0.92, 0.87, 0.82, 0.77, 0.72, 0.67, 0.62, 0.57]
```

## Customization Tips
- Add multiple traces for multi-line charts: `fig.add_trace(go.Scatter(...))`
- Use `px.line(df, x="date", y="value", color="series")` for DataFrames
- Add confidence bands with `fig.add_trace(go.Scatter(fill="tonexty"))`
- Use `fig.add_annotation()` to label specific data points

## Related
- [[Line Chart]] — chart type reference
- [[Line Chart — D3 Template]] — D3.js alternative
