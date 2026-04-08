---
title: Donut Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: donut-chart
library: plotly
---

# Donut Chart — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Donut Chart — Plotly Starter
# Data format: lists of labels and values

labels = ["Coal", "Gas", "Solar", "Wind", "Hydro", "Nuclear"]
values = [1042, 68, 113, 82, 162, 47]
colors = ["#4a4a4a", "#7eb0d5", "#f7c948", "#5ab47a", "#3a86a8", "#9b59b6"]

fig = go.Figure(go.Pie(
    labels=labels,
    values=values,
    hole=0.45,                 # donut hole size (0 = pie, 1 = ring)
    marker=dict(
        colors=colors,
        line=dict(color="white", width=2),
    ),
    textinfo="label+percent",
    textposition="outside",
    textfont_size=12,
    hovertemplate="%{label}: %{value} TWh (%{percent})<extra></extra>",
    sort=False,
))

# Center annotation
total = sum(values)
fig.add_annotation(
    text=f"<b>{total:,}</b><br><span style='font-size:12px'>TWh Total</span>",
    x=0.5, y=0.5,
    font_size=22,
    showarrow=False,
)

fig.update_layout(
    title="India Electricity Generation Mix (TWh)",
    height=450,
    showlegend=True,
    legend=dict(orientation="h", y=-0.1),
)

fig.show()
```

## Configuration Options
- `hole` — 0 to 1; 0.4-0.5 is classic donut, 0.7+ is thin ring
- `textposition` — `"inside"`, `"outside"`, `"auto"`, `"none"`
- `pull` — list of floats to explode individual slices
- Center annotation — use `fig.add_annotation()` for KPI text inside the hole

## Energy/Climate Data Example
```python
# India electricity generation by source (TWh)
labels = ["Coal", "Gas", "Solar", "Wind", "Hydro", "Nuclear"]
values = [1042, 68, 113, 82, 162, 47]
```

## Customization Tips
- Use `rotation=90` to start from a different angle
- Add `opacity=0.9` on traces for subtle transparency
- Create nested donuts by adding multiple `go.Pie` traces with different `domain` settings
- Use `scalegroup` to make multiple donuts the same scale for comparison

## Related
- [[Donut Chart]] — chart type reference
- [[Donut Chart — D3 Template]] — D3.js alternative
