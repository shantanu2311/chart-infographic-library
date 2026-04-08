---
title: Bar Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: bar-chart
library: plotly
---

# Bar Chart — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Bar Chart — Plotly Starter
# Data format: lists of categories and values

categories = ["Coal", "Natural Gas", "Solar", "Wind", "Hydro", "Nuclear"]
values = [1042, 68, 113, 82, 162, 47]
colors = ["#4a4a4a", "#7eb0d5", "#f7c948", "#5ab47a", "#3a86a8", "#9b59b6"]

fig = go.Figure(go.Bar(
    y=categories,
    x=values,
    orientation="h",           # horizontal bars
    marker_color=colors,
    text=values,
    textposition="outside",
    textfont_size=12,
))

fig.update_layout(
    title="Electricity Generation by Source (TWh)",
    xaxis_title="TWh",
    yaxis=dict(autorange="reversed"),  # top-to-bottom order
    height=400,
    margin=dict(l=120, r=40, t=50, b=40),
    plot_bgcolor="white",
)

fig.update_xaxes(showgrid=True, gridcolor="#eee")

fig.show()
```

## Configuration Options
- `orientation` — `"h"` for horizontal, `"v"` for vertical bars
- `marker_color` — single color string or list per bar
- `textposition` — `"inside"`, `"outside"`, `"auto"`, `"none"`
- `plot_bgcolor` — background color of the plot area

## Energy/Climate Data Example
```python
# India electricity generation by source (TWh, FY 2023-24)
categories = ["Coal", "Gas", "Solar", "Wind", "Hydro", "Nuclear", "Biomass"]
values = [1042, 68, 113, 82, 162, 47, 53]
```

## Customization Tips
- Sort bars: zip and sort data before plotting for ranked display
- Use `px.bar()` for quick DataFrame-based charts with automatic legends
- Add `fig.add_vline(x=avg, line_dash="dash")` for reference lines
- Use `fig.update_traces(marker_line_width=1, marker_line_color="white")` for borders

## Related
- [[Bar Chart]] — chart type reference
- [[Bar Chart — D3 Template]] — D3.js alternative
