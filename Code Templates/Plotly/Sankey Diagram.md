---
title: Sankey Diagram — Plotly Template
tags:
  - code-template
  - plotly
chart_type: sankey-diagram
library: plotly
---

# Sankey Diagram — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Sankey Diagram — Plotly Starter
# Data format: node labels list + link source/target/value lists (index-based)

node_labels = [
    "Coal", "Natural Gas", "Solar", "Wind",        # 0-3: sources
    "Thermal Plant", "Grid",                         # 4-5: conversion
    "Industry", "Residential", "Transport",          # 6-8: end use
]

node_colors = [
    "#4a4a4a", "#7eb0d5", "#f7c948", "#5ab47a",
    "#d35400", "#3498db",
    "#e74c3c", "#9b59b6", "#1abc9c",
]

fig = go.Figure(go.Sankey(
    arrangement="snap",
    node=dict(
        label=node_labels,
        color=node_colors,
        pad=20,
        thickness=25,
    ),
    link=dict(
        source=[0, 1, 2, 3, 4, 5, 5, 5],
        target=[4, 4, 5, 5, 5, 6, 7, 8],
        value= [500, 200, 120, 80, 650, 400, 300, 150],
        color=[
            "rgba(74,74,74,0.3)", "rgba(126,176,213,0.3)",
            "rgba(247,201,72,0.3)", "rgba(90,180,122,0.3)",
            "rgba(211,84,0,0.3)",
            "rgba(52,152,219,0.3)", "rgba(52,152,219,0.3)", "rgba(52,152,219,0.3)",
        ],
    ),
))

fig.update_layout(
    title="Energy Flow: Sources to End Use (TWh)",
    height=450,
    font_size=12,
)

fig.show()
```

## Configuration Options
- `node.pad` — vertical spacing between nodes
- `node.thickness` — width of node bars
- `arrangement` — `"snap"` (draggable, snaps), `"fixed"`, `"freeform"`, `"perpendicular"`
- `link.color` — use rgba for transparency on flow bands

## Energy/Climate Data Example
```python
# Energy flow in an industrial facility
node_labels = [
    "Grid Electricity", "Natural Gas", "Diesel",  # inputs
    "EAF", "Induction Furnace", "Boiler",          # processes
    "Steel Product", "Heat Loss", "Emissions",      # outputs
]
source = [0, 1, 2, 0, 3, 4, 5, 3, 4, 5]
target = [3, 5, 4, 4, 6, 6, 6, 8, 7, 8]
value  = [300, 150, 80, 200, 250, 180, 100, 50, 100, 50]
```

## Customization Tips
- Use `hovertemplate` on links for custom tooltip format
- Color links by source node using `node_colors[source_idx]` with alpha
- Add units in hover: `hovertemplate="Flow: %{value} TWh<extra></extra>"`
- For circular flows, Plotly Sankey does not support cycles (use D3 d3-sankey-circular)

## Related
- [[Sankey Diagram]] — chart type reference
- [[Sankey Diagram — D3 Template]] — D3.js alternative
