---
title: Stacked Bar Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: stacked-bar-chart
library: plotly
---

# Stacked Bar Chart — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Stacked Bar Chart — Plotly Starter
# Data format: long-form DataFrame with group, category, and value columns

df = pd.DataFrame({
    "Facility": ["EAF Unit"] * 3 + ["Induction"] * 3 + ["Re-rolling"] * 3 + ["Forge Shop"] * 3,
    "Scope": ["Scope 1", "Scope 2", "Scope 3"] * 4,
    "tCO2e": [
        3200, 2100, 1800,    # EAF
        2500, 3400, 1200,    # Induction
        1800, 1600, 2200,    # Re-rolling
        4100, 2800, 900,     # Forge
    ],
})

fig = px.bar(
    df,
    x="Facility",
    y="tCO2e",
    color="Scope",
    barmode="stack",
    color_discrete_map={
        "Scope 1": "#e63946",
        "Scope 2": "#457b9d",
        "Scope 3": "#2a9d8f",
    },
    title="Emissions by Facility and Scope (tCO2e)",
    text_auto=True,
)

fig.update_layout(
    height=450,
    plot_bgcolor="white",
    legend=dict(orientation="h", y=-0.15),
    yaxis_title="tCO2e",
)

fig.update_xaxes(showgrid=False)
fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `barmode` — `"stack"` for stacked, `"group"` for side-by-side, `"relative"` for pos/neg stacking
- `text_auto` — `True` to auto-format value labels, or format string like `".2s"`
- `barnorm` — `"percent"` for 100% stacked bars
- `orientation` — `"v"` (default) or `"h"` for horizontal

## Energy/Climate Data Example
```python
# Emissions by facility and scope
df = pd.DataFrame({
    "Facility": ["EAF Unit"] * 3 + ["Induction"] * 3 + ["Re-rolling"] * 3,
    "Scope": ["Scope 1", "Scope 2", "Scope 3"] * 3,
    "tCO2e": [3200, 2100, 1800, 2500, 3400, 1200, 1800, 1600, 2200],
})
```

## Customization Tips
- Use `go.Bar()` traces for full control over each stack segment
- Add total labels above bars using `fig.add_annotation()` per group
- Use `barnorm="percent"` for proportional comparison across groups
- Combine with `facet_col` for small multiples by another dimension

## Related
- [[Stacked Bar Chart]] — chart type reference
- [[Stacked Bar Chart — D3 Template]] — D3.js alternative
