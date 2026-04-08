---
title: Pie Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: pie-chart
library: plotly
---

# Pie Chart — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Pie Chart — Plotly Starter
# Data format: lists of labels and values

labels = ["Scope 1 — Direct", "Scope 2 — Electricity", "Scope 3 — Value Chain"]
values = [4500, 3200, 2100]
colors = ["#e63946", "#457b9d", "#2a9d8f"]

fig = go.Figure(go.Pie(
    labels=labels,
    values=values,
    marker=dict(colors=colors, line=dict(color="white", width=2)),
    textinfo="label+percent",
    textposition="inside",
    textfont_size=13,
    hoverinfo="label+value+percent",
    sort=False,  # preserve original order
))

fig.update_layout(
    title="GHG Emissions by Scope (tCO2e)",
    height=420,
    showlegend=True,
    legend=dict(orientation="h", y=-0.1),
)

fig.show()
```

## Configuration Options
- `textinfo` — `"label+percent"`, `"value"`, `"label+value"`, `"none"`
- `textposition` — `"inside"`, `"outside"`, `"auto"`
- `pull` — list of floats to "explode" slices (e.g., `[0.1, 0, 0]` pulls first slice)
- `sort` — `True` to auto-sort by value, `False` to preserve data order

## Energy/Climate Data Example
```python
# Emission breakdown by scope
labels = ["Scope 1 — Direct", "Scope 2 — Electricity", "Scope 3 — Value Chain"]
values = [4500, 3200, 2100]
```

## Customization Tips
- Use `px.pie(df, names="label", values="value")` for DataFrame input
- Add `hole=0.4` to convert to donut chart (see Donut Chart template)
- Use `pull=[0.05, 0, 0]` to emphasize a specific slice
- Customize hover with `hovertemplate="%{label}: %{value} tCO2e (%{percent})<extra></extra>"`

## Related
- [[Pie Chart]] — chart type reference
- [[Pie Chart — D3 Template]] — D3.js alternative
