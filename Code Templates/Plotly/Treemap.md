---
title: Treemap — Plotly Template
tags:
  - code-template
  - plotly
chart_type: treemap
library: plotly
---

# Treemap — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.express as px
import pandas as pd

# Treemap — Plotly Starter
# Data format: DataFrame with path hierarchy columns and a values column

df = pd.DataFrame({
    "Scope": ["Scope 1"] * 4 + ["Scope 2"] * 1 + ["Scope 3"] * 3,
    "Source": [
        "Natural Gas Combustion", "Diesel Generators", "Process CO2", "Fugitive SF6",
        "Grid Electricity",
        "Purchased Goods", "Upstream Transport", "Waste Disposal",
    ],
    "tCO2e": [1800, 600, 1500, 200, 3200, 1100, 450, 320],
})

fig = px.treemap(
    df,
    path=["Scope", "Source"],  # hierarchy levels
    values="tCO2e",
    color="tCO2e",
    color_continuous_scale="YlOrRd",
    title="GHG Emissions Breakdown (tCO2e)",
)

fig.update_layout(
    height=500,
    margin=dict(t=50, l=10, r=10, b=10),
)

fig.update_traces(
    textinfo="label+value",
    textfont_size=12,
    hovertemplate="<b>%{label}</b><br>%{value} tCO2e<br>%{percentParent:.1%} of parent<extra></extra>",
)

fig.show()
```

## Configuration Options
- `path` — list of column names defining the hierarchy (top to bottom)
- `color` — column for color encoding; use `color_continuous_scale` for numeric
- `branchvalues` — `"total"` (parent = sum of children) or `"remainder"`
- `maxdepth` — limit visible depth levels (e.g., 2 to hide leaf nodes initially)

## Energy/Climate Data Example
```python
# Emissions by scope and source category
df = pd.DataFrame({
    "Scope": ["Scope 1"] * 4 + ["Scope 2"] + ["Scope 3"] * 3,
    "Source": [
        "Stationary Combustion", "Mobile Combustion", "Process", "Fugitive",
        "Purchased Electricity",
        "Purchased Goods", "Transport", "Waste",
    ],
    "tCO2e": [1800, 600, 1500, 200, 3200, 1100, 450, 320],
})
```

## Customization Tips
- Use `color_discrete_map` with a categorical color column for custom scope colors
- Add a third hierarchy level: `path=["Total", "Scope", "Source"]`
- Use `px.sunburst()` with the same data for a radial alternative
- Set `fig.update_traces(root_color="lightgrey")` to style the root tile

## Related
- [[Treemap]] — chart type reference
- [[Treemap — D3 Template]] — D3.js alternative
