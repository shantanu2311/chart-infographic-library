---
title: Axis Design
tags:
  - design-principle
  - axes
  - scales
  - formatting
---

# Axis Design

## The Principle
Axes are the coordinate system that gives data meaning. Effective axis design means choosing the right scale (linear, log, time), starting point (zero or not), tick density, and label format so that the reader interprets magnitudes and trends correctly without distortion or confusion.

## Why It Matters
A truncated y-axis on a bar chart can make a 2% difference look like a 200% difference. A logarithmic scale without labeling can mislead readers unfamiliar with exponential data. Dual y-axes create false correlations. Axis design choices directly affect whether a chart tells the truth or lies visually. These are the highest-stakes design decisions you make.

## Key Guidelines
- **Bar charts must start at zero** -- the entire bar length represents the value; truncation distorts magnitude
- **Line charts may start above zero** when showing variation around a level (e.g., temperature anomalies, stock prices)
- Use **logarithmic scales** when data spans multiple orders of magnitude (1 to 1,000,000); always label tick marks clearly
- Avoid **dual y-axes** unless both series share a clear causal relationship AND you clearly label each axis with matching color
- Set tick density to **5-7 ticks** per axis; more creates clutter, fewer loses precision
- Format time axes with **appropriate granularity**: years for decade spans, months for year spans, days for week spans
- Include **units in axis labels** once (e.g., "Emissions (tCO2e)") rather than repeating units on every tick mark
- Use **axis breaks** (zigzag markers) sparingly and only when a single outlier compresses the rest of the data

## Examples

### Good Practice
> [!tip] Do This
> - Bar chart of emission reductions: y-axis starts at zero, tick marks at 0, 200, 400, 600, 800 tCO2e
> - Line chart of temperature anomalies: y-axis centered on zero with +/- range, clear horizontal reference at 0.0
> - Log-scale scatter plot of facility capacity vs emissions: tick marks at 10, 100, 1K, 10K with explicit log-scale note

### Bad Practice
> [!warning] Avoid This
> - Bar chart with y-axis starting at 95 to exaggerate a 5-point difference between categories
> - Dual-axis chart implying correlation between CO2 emissions and GDP by aligning their scales to cross at a specific point
> - Time axis showing "2020, 2021, 2022, 2023, 2024" for monthly data -- too few ticks, hiding seasonal patterns

## Energy & Climate Applications
- Emission values: use TWh for national-scale electricity, GWh for state-scale, MWh for facility-scale -- match unit to magnitude
- tCO2e formatting: use "tCO2e" for facility-level, "MtCO2e" for national, "GtCO2e" for global -- never mix in one chart
- Indian financial year axes: label as "FY22-23" or "FY23" consistently; place tick at April (start of FY)

## Applicable Chart Types
- [[Bar Chart]] -- zero baseline is non-negotiable; horizontal bars for long category labels
- [[Line Chart]] -- flexible baseline; time axis formatting critical for trend readability
- [[Scatter Plot]] -- both axes carry meaning; log scales common for skewed distributions
- [[Waterfall Chart]] -- dynamic x-axis domain `[0, max * 1.08]` for headroom above tallest bar
- [[Area Chart]] -- zero baseline required (area encodes cumulative magnitude)
- [[Histogram]] -- bin width on x-axis determines the chart's message; label bin edges clearly

## Tools & Implementation
- **d3-scale** -- linear, log, time, and band scales with automatic tick generation
- **Recharts `domain` prop** -- set explicit axis domains `[0, 'dataMax']` to enforce zero baseline
- **Datawrapper axis controls** -- GUI for setting range, tick count, format, and log scale toggle

## Further Reading
- [How to Read (and Mislead with) Axes (Datawrapper)](https://blog.datawrapper.de/baselines/) -- comprehensive axis baseline guide
- [Dual-Axis Charts: Why They're Almost Always Wrong (Stephen Few)](https://www.perceptualedge.com/articles/visual_business_intelligence/dual-scaled_axes.pdf) -- the case against dual axes

## Related Principles
- [[Data-Ink Ratio]]
- [[Typography in Charts]]
- [[Annotation Techniques]]
- [[Legend Placement]]
