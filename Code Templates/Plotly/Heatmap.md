---
title: Heatmap — Plotly Template
tags:
  - code-template
  - plotly
chart_type: heatmap
library: plotly
---

# Heatmap — Plotly

## Setup
```bash
pip install plotly numpy
```

## Basic Template (Python)
```python
import plotly.graph_objects as go
import numpy as np

# Heatmap — Plotly Starter
# Data format: 2D array (z) with x labels (columns) and y labels (rows)

months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
          "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
sources = ["Solar", "Wind", "Hydro"]

# Capacity factor (%) by month and source
z = [
    [12, 18, 28, 45, 52, 48, 42, 38, 35, 30, 15, 10],  # Solar
    [35, 30, 22, 18, 15, 20, 25, 22, 28, 32, 38, 36],  # Wind
    [25, 22, 18, 15, 30, 42, 50, 55, 45, 35, 28, 26],  # Hydro
]

fig = go.Figure(go.Heatmap(
    z=z,
    x=months,
    y=sources,
    colorscale="YlOrRd",
    text=z,
    texttemplate="%{text}%",
    textfont_size=11,
    hovertemplate="Month: %{x}<br>Source: %{y}<br>Capacity: %{z}%<extra></extra>",
    colorbar=dict(title="Capacity %"),
))

fig.update_layout(
    title="Monthly Capacity Factor by Renewable Source (%)",
    height=350,
    xaxis_title="Month",
    yaxis_title="Energy Source",
    yaxis=dict(autorange="reversed"),
)

fig.show()
```

## Configuration Options
- `colorscale` — `"YlOrRd"`, `"Blues"`, `"Viridis"`, `"RdYlGn"` (diverging), or custom
- `texttemplate` — format text inside cells (e.g., `"%{text:.1f}"`)
- `zmin` / `zmax` — fix color scale range instead of auto
- `xgap` / `ygap` — pixel gap between cells (e.g., `2`)

## Energy/Climate Data Example
```python
# Monthly renewable capacity factor (%) — India
months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
          "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
sources = ["Solar PV", "Onshore Wind", "Small Hydro"]
z = [
    [12, 18, 28, 45, 52, 48, 42, 38, 35, 30, 15, 10],
    [35, 30, 22, 18, 15, 20, 25, 22, 28, 32, 38, 36],
    [25, 22, 18, 15, 30, 42, 50, 55, 45, 35, 28, 26],
]
```

## Customization Tips
- Use `px.imshow(df)` for quick heatmap from a DataFrame or numpy array
- Add `xgap=2, ygap=2` for visible cell borders
- Use diverging colorscale (`"RdYlGn"`) with `zmid=0` for data centered on zero
- Annotate only significant cells by conditionally setting text to empty strings

## Related
- [[Heatmap]] — chart type reference
- [[Heatmap — D3 Template]] — D3.js alternative
