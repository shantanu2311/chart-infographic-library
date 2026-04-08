---
title: Dot Plot
aliases:
  - Cleveland Dot Plot
  - Dot Chart
tags:
  - chart-type/comparison
  - data-type/categorical
  - data-type/numeric
  - complexity/beginner
  - audience/analyst
  - audience/executive
  - audience/researcher
  - theme/energy-markets
  - theme/renewable-energy
  - theme/carbon-markets
  - theme/climate
  - theme/iea
category: Comparison
complexity: beginner
best_audience: analyst, executive, researcher
---

# Dot Plot

## What It Is
A dot plot places a single dot along a numeric axis for each category, enabling precise value reading and clean comparison across many items. Championed by statistician William Cleveland for its superior perceptual accuracy compared to bar charts, the dot plot strips away unnecessary ink and lets the data speak. It is particularly effective when the goal is to compare exact values rather than emphasise magnitude through bar length.

## Best Data Types
- Categorical data paired with a single continuous numeric measure
- Data where precise value reading matters more than visual impact
- Large numbers of categories (20-60+) where bars would create visual clutter
- Metrics such as rates, prices, indices, or efficiency scores
- Comparative data across entities (countries, facilities, technologies)

## When to Use
- Comparing a single metric across many categories with minimal visual noise
- When exact value reading and ranking clarity are priorities
- Displaying data in academic, technical, or research-oriented reports
- Replacing bar charts when the chart feels heavy or cluttered
- Showing distributions of a metric across groups when a full distribution chart is overkill

## When NOT to Use
> [!warning] Avoid When
> - You need to show composition or part-to-whole relationships
> - The audience expects a more familiar chart type and may not understand dot plots
> - You want to emphasise the magnitude of differences (bars provide stronger visual impact)
> - You need to compare multiple measures per category (use a [[Dumbbell Chart]] or [[Bullet Chart]])
> - Data points are so close together that dots overlap and become unreadable

## Real-World Use Cases
- Country rankings by Human Development Index
- Hospital performance ratings across quality metrics
- University research output scores
- City-level air quality index comparisons

### Energy & Climate Applications
- Levelized cost of energy (LCOE) by technology across 20+ options (IEA World Energy Outlook data)
- Carbon credit prices across voluntary market registries (Verra VCS, Gold Standard, ACR, CORSIA-eligible)
- Grid emission factors by region across India (Northern, Western, Southern, Eastern, North-Eastern grids)
- Electricity tariffs by state for industrial consumers (CERC/SERC rate orders)
- Critical mineral reserves by country (lithium in Chile, Australia, Argentina; cobalt in DRC; nickel in Indonesia)

## Visual Style Variations
- **Horizontal dot plot** — categories on y-axis with dots along x-axis; the classic Cleveland format
- **Colour-grouped dots** — dot colour encodes a grouping variable (e.g., region, technology type)
- **Dot plot with reference line** — a vertical line marks a benchmark (e.g., global average LCOE) for context
- **Sized dots** — dot diameter encodes a second variable (e.g., market share alongside price)

## Related Charts
- [[Lollipop Chart]] — adds a connecting line from axis to dot for stronger visual anchoring
- [[Scatter Plot]] — plots two numeric variables against each other rather than category vs value
- [[Bar Chart]] — the heavier alternative when visual impact matters more than precision
- [[Dumbbell Chart]] — extends the dot plot to show paired values (before/after, min/max)

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IEA World Energy Outlook](https://www.iea.org/reports/world-energy-outlook-2024) — LCOE and cost comparison charts
- [William Cleveland — The Elements of Graphing Data](https://en.wikipedia.org/wiki/William_S._Cleveland) — foundational reference for dot plots
