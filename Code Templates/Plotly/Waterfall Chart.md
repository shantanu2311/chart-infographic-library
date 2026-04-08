---
title: Waterfall Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: waterfall-chart
library: plotly
---

# Waterfall Chart — Plotly

## Setup
```bash
pip install plotly
```

## Basic Template (Python)
```python
import plotly.graph_objects as go

# Waterfall Chart — Plotly Starter
# Data format: lists of labels, measures ("relative"/"total"/"absolute"), and values

labels = ["Baseline", "Energy Eff.", "Solar PV", "Fuel Switch",
          "Process Opt.", "Prod. Increase", "Net Emissions"]

measures = ["absolute", "relative", "relative", "relative",
            "relative", "relative", "total"]

values = [10000, -1200, -1800, -800, -500, 600, 0]  # total auto-calculated

fig = go.Figure(go.Waterfall(
    x=labels,
    y=values,
    measure=measures,
    text=[f"{v:+,}" if m == "relative" else f"{v:,}" for v, m in zip(values, measures)],
    textposition="outside",
    textfont_size=11,
    connector=dict(line=dict(color="#999", dash="dot")),
    decreasing=dict(marker=dict(color="#2a9d8f")),  # green for reductions
    increasing=dict(marker=dict(color="#e63946")),   # red for increases
    totals=dict(marker=dict(color="#457b9d")),        # blue for totals
))

fig.update_layout(
    title="Emission Reduction Waterfall (tCO2e/year)",
    yaxis_title="tCO2e",
    height=450,
    plot_bgcolor="white",
    showlegend=False,
)

fig.update_yaxes(showgrid=True, gridcolor="#f0f0f0")

fig.show()
```

## Configuration Options
- `measure` — `"absolute"` (fixed bar), `"relative"` (floating delta), `"total"` (running sum)
- `decreasing.marker.color` — color for negative changes
- `increasing.marker.color` — color for positive changes
- `connector.line` — style of connector lines between bars (dash, color, width)

## Energy/Climate Data Example
```python
# Emission reduction pathway for an MSME steel plant
labels = ["Current", "VFD Motors", "Rooftop Solar", "PNG Switch",
          "Waste Heat Recovery", "BESS + Solar", "Target"]
measures = ["absolute", "relative", "relative", "relative",
            "relative", "relative", "total"]
values = [10000, -1200, -1800, -800, -500, -1500, 0]
```

## Customization Tips
- The `"total"` measure auto-calculates the running sum — set value to `0` or any placeholder
- Use `texttemplate` for custom formatting: `"%{text} tCO2e"`
- Add a target line with `fig.add_hline(y=target, line_dash="dash", annotation_text="Target")`
- Rotate x-axis labels: `fig.update_xaxes(tickangle=-30)` for long names

## Related
- [[Waterfall Chart]] — chart type reference
- [[Waterfall Chart — D3 Template]] — D3.js alternative
