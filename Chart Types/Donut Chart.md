---
title: Donut Chart
aliases:
  - Doughnut Chart
  - Ring Chart
chart_type: donut-chart
category: part-to-whole
data_types:
  - categorical
  - proportional
data_contexts:
  - Energy Markets
  - Renewable Energy & Transition
  - ESG & Sustainable Finance
complexity: simple
audience:
  - executive
  - public
visual_styles:
  - corporate
  - minimal
  - dashboard
color_approach: categorical
libraries:
  - d3
  - plotly
  - chartjs
  - echarts
  - recharts
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/composition
  - data-type/categorical
  - data-type/proportional
  - complexity/beginner
  - audience/general-public
  - audience/executives
  - audience/dashboard-users
  - theme/renewable-energy
  - theme/emissions
  - theme/climate-finance
---

# Donut Chart

## What It Is
A donut chart is a variant of the [[Pie Chart]] with a hollow center, creating a ring shape. The empty center can be used to display a key metric, label, or icon, making it a popular choice for dashboards and KPI displays. The ring format also reduces emphasis on area comparison, which can slightly improve readability over a traditional pie chart.

## Best Data Types
- Parts-of-whole with 2-5 categories
- Percentages or proportions summing to 100%
- Binary or ternary splits (e.g., renewable vs non-renewable)
- Single-snapshot composition data paired with a headline number

## When to Use
- Displaying a headline KPI in the center (e.g., "72% renewable") with supporting breakdown in the ring
- Dashboard widgets where space is constrained
- Comparing a simple two-way or three-way split
- When the center annotation adds meaningful context that a pie chart cannot provide
- Pairing with other donut charts in a small-multiples layout for comparison

## When NOT to Use
> [!warning] Avoid When
> - You have more than 5-6 categories (ring segments become too thin to distinguish)
> - Precise value comparison between similar-sized segments is required
> - You need to show change over time (use a [[Stacked Bar Chart]] or area chart instead)
> - Nested donuts are stacked too deep, creating confusion (prefer a [[Sunburst Chart]] for hierarchy)
> - The data does not represent parts of a whole

## Real-World Use Cases
- Website analytics: traffic source split with total visits in the center
- HR dashboards: employee demographics with headcount displayed centrally
- Financial reports: expense breakdown with total spend in the center
- Health metrics: macronutrient split with total calories shown

### Energy & Climate Applications
- Renewable vs non-renewable share of national electricity generation with total TWh in center
- Scope 1, Scope 2, and Scope 3 emissions breakdown with total tCO2e displayed centrally
- Climate finance split: public vs private sources with total USD committed in center
- COP pledged finance: adaptation vs mitigation with total pledge amount
- NDC progress: on-track vs off-track vs insufficient, with number of countries in center

## Visual Style Variations
- **Standard donut** — single ring with center KPI and segment labels
- **Nested donut** — concentric rings showing two levels of hierarchy (use sparingly)
- **Half donut / gauge** — semi-circular ring used as a progress indicator
- **Thin ring** — minimalist style with a very narrow band, popular in modern dashboards

## Related Charts
- [[Pie Chart]] — the solid predecessor; use when center annotation is not needed
- [[Sunburst Chart]] — multi-ring hierarchical version for deeper categorical drill-down
- [[Waffle Chart]] — grid-based alternative that avoids angle-perception issues

## Inspiration Sources
- [IRENA Renewable Energy Statistics](https://www.irena.org/publications) — renewable share visualizations
- [Climate Policy Initiative - Global Landscape of Climate Finance](https://www.climatepolicyinitiative.org/) — public vs private climate finance donuts
- [GHG Protocol Corporate Standard](https://ghgprotocol.org/) — Scope 1/2/3 breakdown reporting
