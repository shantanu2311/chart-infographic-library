---
title: Dumbbell Chart
aliases:
  - Connected Dot Plot
  - Dumbbell Plot
  - Gap Chart
tags:
  - chart-type/comparison
  - data-type/paired-comparisons
  - data-type/numeric
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/policymaker
  - theme/climate
  - theme/energy-markets
  - theme/renewable-energy
  - theme/carbon-markets
  - theme/net-zero
  - theme/cop-unfccc
category: Comparison
complexity: intermediate
best_audience: analyst, executive, policymaker
---

# Dumbbell Chart

## What It Is
A dumbbell chart displays two data points per category connected by a line, creating a visual resemblance to a dumbbell or barbell. It is designed to highlight the gap, change, or difference between two related values for each category. The connecting line draws attention to the magnitude and direction of the difference, making it an excellent tool for before/after comparisons, target vs actual tracking, and disparity analysis.

## Best Data Types
- Paired numeric values per category (start/end, before/after, target/actual)
- Change over two time points for multiple categories
- Gap analysis between two groups, scenarios, or conditions
- Comparative metrics where the distance between values is the story
- Policy impact assessment (pre-intervention vs post-intervention)

## When to Use
- Showing change between two time points across many categories simultaneously
- Highlighting which categories have the largest or smallest gaps
- Comparing two scenarios or conditions (e.g., BAU vs net-zero pathway)
- Displaying before/after impact of a policy, technology, or intervention
- When you want to convey both the absolute positions and the relative gap

## When NOT to Use
> [!warning] Avoid When
> - You have more than two data points per category (use a slope chart or line chart)
> - The two values are nearly identical for all categories (the chart will look flat and uninformative)
> - You need to show distributions rather than point values (use a [[Box Plot]] or [[Violin Plot]])
> - Categories are too numerous (beyond 25-30) and the chart becomes a wall of lines
> - The story is about trends over multiple time periods rather than a two-point comparison

## Real-World Use Cases
- Gender pay gap by industry (male vs female median salary)
- Poverty rates before and after a social programme
- Customer satisfaction scores at start vs end of a service improvement initiative
- Test scores pre-training vs post-training across departments

### Energy & Climate Applications
- Before/after Paris Agreement emissions by country (2015 baseline vs latest reported year)
- Fossil fuel LCOE vs renewable LCOE change over a decade (IEA/IRENA cost data)
- Carbon price in 2020 vs 2025 across compliance markets (EU ETS, UK ETS, China, Korea, RGGI)
- Pledged vs delivered climate finance by developed countries (USD 100 billion goal tracking)
- Energy intensity of GDP: 2010 vs 2024 by G20 country (IEA Energy Efficiency indicators)

## Visual Style Variations
- **Horizontal dumbbell** — categories on y-axis, value axis horizontal; best for long category names
- **Colour-coded endpoints** — different colours for the two dots (e.g., blue for baseline, green for current)
- **Arrow dumbbell** — the connecting line includes an arrowhead showing direction of change
- **Sorted dumbbell** — sorted by gap size to highlight largest improvements or widenings at the top

## Related Charts
- [[Slope Chart]] — connects values across two vertical axes; emphasises direction and steepness of change
- [[Lollipop Chart]] — shows a single value per category; the dumbbell extends this to paired values
- [[Bullet Chart]] — compares actual vs target with qualitative ranges in a more compact format
- [[Dot Plot]] — the single-point ancestor of the dumbbell chart

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IRENA Renewable Power Generation Costs](https://www.irena.org/publications) — cost change comparisons across technologies
- [Climate Finance Delivery Plan Progress Reports](https://www.oecd.org/en/topics/climate-finance.html) — pledge vs delivery gap analysis
