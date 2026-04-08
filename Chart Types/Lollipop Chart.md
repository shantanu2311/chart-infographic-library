---
title: Lollipop Chart
aliases:
  - Lollipop Plot
tags:
  - chart-type/comparison
  - data-type/categorical
  - data-type/numeric
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - theme/climate
  - theme/renewable-energy
  - theme/net-zero
  - theme/cop-unfccc
  - theme/energy-markets
category: Comparison
complexity: intermediate
best_audience: analyst, executive
---

# Lollipop Chart

## What It Is
A lollipop chart combines a thin line (the stick) with a dot (the lollipop head) at the end to represent a data value for each category. It conveys the same information as a [[Bar Chart]] but with significantly less visual weight, making it easier to scan when many categories are displayed. The dot draws the eye to the precise value while the line provides a clear visual connection to the axis.

## Best Data Types
- Categorical data with a single numeric measure
- Ranked or ordered values across many categories (20-50+)
- Data where precise endpoint reading is important
- Single-variable comparisons where ink-to-data ratio matters
- Performance scores, indices, or ratings

## When to Use
- Ranking a large number of categories where bar charts feel heavy
- Displaying scores, indices, or single-metric performance measures
- When you want a cleaner, more modern aesthetic than a bar chart
- Highlighting outliers in a long list of categories
- Presenting data in reports or publications where visual elegance matters

## When NOT to Use
> [!warning] Avoid When
> - You need to show composition or stacked values (lollipops cannot be stacked effectively)
> - The audience is unfamiliar with this chart type (bar charts are more universally understood)
> - You have very few categories (under 5) where a bar chart is simpler and clearer
> - You need to compare multiple measures per category (use grouped bars or a [[Bullet Chart]])
> - Data values are very similar, making dot positions hard to distinguish

## Real-World Use Cases
- University rankings by overall score
- Customer NPS scores across product lines
- Country rankings by a governance or development index
- Employee performance ratings across departments

### Energy & Climate Applications
- Emission intensity rankings across 30+ countries (tCO2e per unit GDP) for COP benchmarking
- Levelized cost of energy (LCOE) comparison across 15+ technologies (IEA, IRENA, Lazard)
- Country NDC ambition scores as assessed by Climate Action Tracker
- Energy efficiency improvement rates by industrial sub-sector (BEE PAT scheme data)
- Critical mineral price rankings (lithium, cobalt, nickel, copper, rare earths) for energy transition supply chain analysis

## Visual Style Variations
- **Horizontal lollipop** — categories on y-axis, values extending right; best for long category names
- **Vertical lollipop** — categories on x-axis, values extending up; works for time-ordered categories
- **Colour-coded dots** — dot colour encodes a second variable (e.g., region or performance tier)
- **Diverging lollipop** — sticks extend left and right from a central baseline to show above/below average performance

## Related Charts
- [[Dot Plot]] — removes the stick entirely, focusing purely on dot position
- [[Bar Chart]] — the heavier but more universally recognised alternative
- [[Bullet Chart]] — adds target and qualitative range context to a single-measure comparison
- [[Dumbbell Chart]] — uses two dots per category to show change or gap

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Climate Action Tracker](https://climateactiontracker.org/) — country rating visualisations
- [Lazard LCOE Analysis](https://www.lazard.com/research-insights/) — energy cost comparison charts
