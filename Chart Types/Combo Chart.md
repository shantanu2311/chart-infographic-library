---
title: Combo Chart
aliases:
  - Dual-Axis Chart
  - Mixed Chart
  - Overlay Chart
tags:
  - chart-type/multi-measure
  - data-type/time-series
  - data-type/quantitative
  - data-type/mixed-units
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/operations
  - theme/energy
  - theme/climate
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/finance
category: Multi-measure
complexity: intermediate
best_audience: analysts, executives, operations managers
---

# Combo Chart

## What It Is
A combo chart overlays two or more chart types (typically bars and lines) on a shared x-axis, often with dual y-axes to accommodate different units or scales. This allows two related but differently-scaled metrics to be visualized together, revealing correlations, divergences, and cause-effect patterns that would be invisible in separate charts. It is one of the most widely used chart types in business and energy analytics dashboards.

## Best Data Types
- Two metrics sharing a time axis but with different units (e.g., price in USD + volume in MWh)
- A volume/quantity metric (bars) paired with a rate/ratio metric (line)
- Primary metric with an overlay of a secondary trend or target line
- Budget (bars) vs. actuals (line), or capacity (bars) vs. utilization (line)

## When to Use
- Showing how a rate metric relates to a volume metric over time
- Carbon price (line) overlaid on trading volume (bars) for market analysis
- Comparing actual values (bars) against a trend or target (line)
- When two metrics have different units but a shared time dimension
- Dashboard views where space efficiency matters

## When NOT to Use
> [!warning] Avoid When
> - The two y-axes have no meaningful relationship (dual axes can mislead)
> - Both metrics share the same unit and scale (just use a grouped [[Bar Chart]] or multi-line [[Line Chart]])
> - The audience may misinterpret the dual axes as implying causation
> - More than 3 overlaid series are needed (chart becomes cluttered)
> - The scales can be manipulated to suggest false correlations (use with integrity)

## Real-World Use Cases
- Revenue (bars) vs. profit margin (line) in quarterly financial reports
- Temperature (line) vs. precipitation (bars) in weather dashboards
- Website visits (bars) vs. conversion rate (line) in marketing analytics
- Production volume (bars) vs. defect rate (line) in manufacturing QC

### Energy & Climate Applications
- Carbon price per tonne (line) vs. ETS trading volume (bars) showing market dynamics
- Renewable installed capacity in GW (bars) vs. LCOE decline in USD/MWh (line)
- GDP growth rate (line) vs. absolute emissions (bars) illustrating decoupling
- Monthly rainfall (bars) vs. hydroelectric generation (line) showing correlation
- Electricity demand in MW (bars) vs. spot price in INR/kWh (line) for grid economics

## Visual Style Variations
- **Bar + line** — the classic combo; bars for volume, line for rate
- **Stacked bar + line** — stacked composition bars with an overlaid trend line
- **Area + line** — filled area for one metric, line for another
- **Bar + bar (dual axis)** — two bar series on different scales (less common, more confusing)

## Related Charts
- [[Line Chart]] — pure line version when both metrics share units
- [[Bar Chart]] — pure bar version for single-metric categorical comparison
- [[Area Chart]] — filled alternative to the line component for volume emphasis

## Tools That Support This
- **Excel** — native combo chart type with secondary axis option
- **Tableau** — dual-axis via "Dual Axis" on Columns/Rows shelf
- **Power BI** — line and clustered column combo chart
- **Recharts** — `ComposedChart` component combining Bar, Line, and Area

## Inspiration Sources
- [Recharts ComposedChart API](https://recharts.org/en-US/api/ComposedChart) — React implementation for combo charts
- [Tableau Dual Axis Guide](https://www.tableau.com/blog) — best practices for dual-axis charts
