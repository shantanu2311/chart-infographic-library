---
title: Candlestick Chart — Plotly Template
tags:
  - code-template
  - plotly
chart_type: candlestick-chart
library: plotly
---

# Candlestick Chart — Plotly

## Setup
```bash
pip install plotly pandas
```

## Basic Template (Python)
```python
import plotly.graph_objects as go
import pandas as pd

# Candlestick Chart — Plotly Starter
# Data format: DataFrame with date, open, high, low, close columns

df = pd.DataFrame({
    "Date": pd.to_datetime([
        "2024-01-02", "2024-01-03", "2024-01-04", "2024-01-05",
        "2024-01-08", "2024-01-09", "2024-01-10", "2024-01-11",
        "2024-01-12", "2024-01-15", "2024-01-16", "2024-01-17",
    ]),
    "Open":  [72.5, 74.3, 77.1, 75.2, 73.0, 75.5, 79.8, 81.0, 78.2, 79.5, 82.0, 84.5],
    "High":  [76.0, 78.2, 79.0, 77.5, 75.8, 80.2, 82.5, 83.0, 80.0, 84.0, 86.0, 87.2],
    "Low":   [70.1, 73.5, 74.0, 72.0, 71.5, 75.0, 78.0, 77.5, 76.0, 79.0, 81.0, 83.0],
    "Close": [74.3, 77.1, 75.2, 73.0, 75.5, 79.8, 81.0, 78.2, 79.5, 83.2, 85.5, 84.0],
})

fig = go.Figure(go.Candlestick(
    x=df["Date"],
    open=df["Open"],
    high=df["High"],
    low=df["Low"],
    close=df["Close"],
    increasing=dict(line=dict(color="#22c55e"), fillcolor="#22c55e"),
    decreasing=dict(line=dict(color="#ef4444"), fillcolor="#ef4444"),
    name="EU ETS Carbon Price",
))

fig.update_layout(
    title="EU Carbon Credit Price (EUR/tCO2)",
    yaxis_title="EUR/tCO2",
    xaxis_title="Date",
    height=450,
    xaxis_rangeslider_visible=False,  # hide range slider
    plot_bgcolor="white",
)

fig.update_xaxes(showgrid=True, gridcolor="#f5f5f5")
fig.update_yaxes(showgrid=True, gridcolor="#f5f5f5")

fig.show()
```

## Configuration Options
- `increasing` / `decreasing` — set `line.color` and `fillcolor` for up/down candles
- `xaxis_rangeslider_visible` — `True` for interactive range selector below chart
- `xaxis.rangebreaks` — use `[dict(bounds=["sat", "mon"])]` to skip weekends
- `whiskerwidth` — width of the high-low whiskers (0 to 1)

## Energy/Climate Data Example
```python
# EU ETS carbon credit weekly OHLC (EUR/tCO2)
df = pd.DataFrame({
    "Date": pd.to_datetime(["2024-01-08", "2024-01-15", "2024-01-22", "2024-01-29"]),
    "Open":  [72.5, 74.3, 77.1, 75.2],
    "High":  [76.0, 78.2, 79.0, 77.5],
    "Low":   [70.1, 73.5, 74.0, 72.0],
    "Close": [74.3, 77.1, 75.2, 73.0],
})
```

## Customization Tips
- Add moving average overlay: `fig.add_trace(go.Scatter(x=dates, y=ma, mode="lines"))`
- Add volume bars as a secondary y-axis with `go.Bar` trace
- Use `xaxis.rangebreaks` to remove gaps for non-trading days
- Add `fig.add_hline(y=support_level)` for support/resistance lines

## Related
- [[Candlestick Chart]] — chart type reference
- [[Candlestick Chart — D3 Template]] — D3.js alternative
