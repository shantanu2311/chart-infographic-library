---
title: Radar Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: radar-chart
library: plotly
---

# Radar Chart — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Radar Chart — Plotly Starter
# Data format: list of axis names + values per series (close the polygon by repeating first value)

categories = ["Energy Efficiency", "Renewable Share", "Waste Reduction",
              "Water Recycling", "Process Optimization", "Emission Intensity"]

fig = go.Figure()

# Series 1 — Current performance
fig.add_trace(go.Scatterpolar(
    r=[0.55, 0.30, 0.50, 0.45, 0.60, 0.40, 0.55],  # repeat first value to close
    theta=categories + [categories[0]],
    fill="toself",
    fillcolor="rgba(37, 99, 235, 0.15)",
    line=dict(color="#2563eb", width=2),
    name="Current",
    marker=dict(size=6),
))

# Series 2 — Target
fig.add_trace(go.Scatterpolar(
    r=[0.85, 0.75, 0.80, 0.70, 0.90, 0.80, 0.85],
    theta=categories + [categories[0]],
    fill="toself",
    fillcolor="rgba(230, 57, 70, 0.1)",
    line=dict(color="#e63946", width=2),
    name="Target 2030",
    marker=dict(size=6),
))

fig.update_layout(
    title="Sustainability Performance Scorecard",
    height=500,
    polar=dict(
        radialaxis=dict(
            visible=True,
            range=[0, 1],
            tickvals=[0.2, 0.4, 0.6, 0.8, 1.0],
            ticktext=["20%", "40%", "60%", "80%", "100%"],
        ),
    ),
    showlegend=True,
    legend=dict(x=0.85, y=1.0),
)

fig.show()
```

## Configuration Options
- `fill` — `"toself"` fills the polygon area, `"none"` for lines only
- `polar.radialaxis.range` — set consistent scale across charts
- `polar.angularaxis.direction` — `"clockwise"` or `"counterclockwise"`
- `line.dash` — `"solid"`, `"dash"`, `"dot"` per series

## Energy/Climate Data Example
```python
# Sustainability performance scores (0-1 normalized)
categories = ["Energy Efficiency", "Renewable Share", "Waste Reduction",
              "Water Recycling", "Process Optimization", "Emission Intensity"]
current = [0.55, 0.30, 0.50, 0.45, 0.60, 0.40]
target  = [0.85, 0.75, 0.80, 0.70, 0.90, 0.80]
```

## Customization Tips
- Always repeat the first value at the end of `r` and `theta` to close the polygon
- Normalize all values to 0-1 for fair visual comparison across dimensions
- Use `fig.add_trace()` to overlay multiple series (e.g., before/after, facilities)
- Set `polar.angularaxis.rotation=90` to rotate the starting axis

## Related
- [[Radar Chart]] — chart type reference
- [[Radar Chart — D3 Template]] — D3.js alternative
