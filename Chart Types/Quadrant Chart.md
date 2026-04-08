---
title: Quadrant Chart
aliases:
  - 2x2 Matrix
  - Four Quadrant
  - Boston Matrix
chart_type: quadrant-chart
category: comparison
data_types:
  - continuous
  - paired
data_contexts:
  - Climate Tech & Cleantech Startups
  - Renewable Energy & Transition
  - ESG & Sustainable Finance
complexity: medium
audience:
  - executive
  - technical
  - policymaker
visual_styles:
  - corporate
  - minimal
color_approach: categorical
libraries:
  - d3
  - plotly
  - tableau
  - matplotlib
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/comparison
  - data-type/bivariate
  - data-type/categorical-output
  - data-type/quantitative
  - complexity/intermediate
  - audience/executive
  - audience/analyst
  - audience/policymaker
  - theme/energy
  - theme/climate
  - theme/finance
  - theme/renewable-energy
  - theme/net-zero
  - theme/esg
---

# Quadrant Chart

## What It Is
A quadrant chart is a [[Scatter Plot]] divided into four labeled regions by two perpendicular threshold lines (one vertical, one horizontal). Each data point falls into one of four categories based on whether its x and y values are above or below the respective thresholds. This transforms continuous bivariate data into a strategic 2x2 classification framework — making it a powerful decision-support tool used in BCG matrices, Gartner Magic Quadrants, and priority matrices across industries.

## Best Data Types
- Two continuous metrics per entity with meaningful threshold values for each
- Data where the 2x2 classification drives decisions (invest, divest, monitor, deprioritize)
- Strategic assessment data: cost vs. impact, risk vs. return, urgency vs. feasibility
- Technology or portfolio evaluation across two key dimensions

## When to Use
- Categorizing technologies by cost vs. CO2 reduction potential (cheap+effective is the winner quadrant)
- Investment screening: risk vs. return for clean energy portfolios
- Prioritizing climate policies by urgency vs. feasibility
- Any strategic assessment where a 2x2 framework aids decision-making
- When the quadrant label (e.g., "Quick Win," "Strategic Bet," "Low Priority," "Reconsider") is the takeaway

## When NOT to Use
> [!warning] Avoid When
> - Threshold lines are arbitrary and misleading (quadrant placement must be defensible)
> - The data is not naturally bivariate or the two axes are not independent
> - Most points cluster in one quadrant (the classification adds no value)
> - You need to show trends over time (use [[Connected Scatter Plot]])
> - The audience needs more than 4 categories (add a size/color dimension or use [[Parallel Coordinates]])

## Real-World Use Cases
- BCG Growth-Share Matrix (market growth vs. relative market share)
- Gartner Magic Quadrant (ability to execute vs. completeness of vision)
- Eisenhower Priority Matrix (urgency vs. importance)
- Risk assessment matrices (likelihood vs. impact)

### Energy & Climate Applications
- Technology cost vs. CO2 reduction potential: quadrants labeled "Quick Wins" (low cost, high reduction), "Strategic Bets" (high cost, high reduction), "Low Priority" (high cost, low reduction), "Easy Extras" (low cost, low reduction)
- Risk vs. return for clean energy investment portfolios (debt, equity, project finance)
- Urgency vs. feasibility of climate adaptation policies by sector
- Abatement cost vs. abatement potential (marginal abatement cost curve as a quadrant view)
- ESG score vs. financial performance for portfolio screening

## Visual Style Variations
- **Labeled quadrants** — each quadrant has a strategic label (e.g., "Invest," "Monitor")
- **Bubble quadrant** — bubble size adds a third dimension (e.g., market size or emission volume)
- **Color-coded quadrants** — background shading (green, yellow, orange, red) reinforcing priority
- **Annotated quadrant** — key entities labeled directly on the chart with callouts

## Related Charts
- [[Scatter Plot]] — the base chart without quadrant divisions
- [[Bubble Chart]] — adds a size dimension; can be combined with quadrant lines
- [[Radar Chart]] — multi-axis comparison; use when more than 2 dimensions matter equally

## Tools That Support This
- **Excel** — scatter plot with manually added threshold lines and text boxes
- **Tableau** — reference lines on scatter plot creating quadrant divisions
- **Miro** — 2x2 matrix templates for strategic workshops
- **Power BI** — scatter chart with constant lines for quadrant boundaries

## Inspiration Sources
- [Gartner Magic Quadrant Methodology](https://www.gartner.com/en/research/methodologies/magic-quadrants-research) — the canonical quadrant chart application
- [Tableau Quadrant Chart Tutorial](https://www.tableau.com/blog) — implementation guide with reference lines
