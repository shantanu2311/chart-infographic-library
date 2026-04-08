---
title: Tornado Chart
aliases:
  - Butterfly Chart
  - Diverging Bar Chart
  - Sensitivity Chart
chart_type: tornado-chart
category: comparison
data_types:
  - categorical
  - paired
data_contexts:
  - Climate & Emissions
  - Renewable Energy & Transition
  - Energy Markets
complexity: medium
audience:
  - technical
  - policymaker
visual_styles:
  - corporate
  - data-journalism
color_approach: diverging
libraries:
  - d3
  - plotly
  - matplotlib
  - tableau
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/comparison
  - data-type/categorical
  - data-type/bipolar
  - data-type/scenario
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/policymaker
  - theme/energy
  - theme/climate
  - theme/net-zero
  - theme/finance
---

# Tornado Chart

## What It Is
A tornado chart displays back-to-back horizontal bars extending from a central axis, comparing two opposing groups, scenarios, or directions. Named for its tornado-like silhouette when bars are sorted by magnitude, it excels at sensitivity analysis (showing which variables swing the outcome most) and at contrasting two scenarios or populations side by side. The mirrored layout makes differences immediately visible.

## Best Data Types
- Two opposing measures across the same categories (e.g., BAU vs. net-zero)
- Sensitivity analysis results (high/low impact per variable)
- Before/after comparisons
- Positive/negative divergence from a baseline
- Survey responses (agree vs. disagree by question)

## When to Use
- Comparing two scenarios, policies, or time periods across shared categories
- Sensitivity analysis: ranking which input assumptions most affect the output
- Showing the gap between two groups (e.g., fossil fuel jobs vs. clean energy jobs by region)
- Before/after policy intervention impact visualization
- When the contrast between left and right is the primary insight

## When NOT to Use
> [!warning] Avoid When
> - You have more than two groups to compare (use [[Stacked Bar Chart]] or [[Radar Chart]])
> - Categories are not shared between both sides
> - The data is not naturally bipolar or paired
> - You need to show trends over time (use [[Line Chart]])
> - There are too many categories (more than 15-20 makes the chart unwieldy)

## Real-World Use Cases
- Financial sensitivity analysis (which assumptions most affect NPV)
- Survey results showing agree/disagree splits
- Political polling comparing two candidates by demographic
- HR analytics comparing hiring vs. attrition by department

### Energy & Climate Applications
- BAU vs. net-zero scenario emissions comparison by sector
- Fossil fuel vs. renewable energy employment by region or state
- Before/after policy intervention emissions (e.g., carbon tax impact by industry)
- Sensitivity analysis of Levelized Cost of Energy (LCOE) assumptions (discount rate, capacity factor, fuel cost, CAPEX)
- Import vs. export volumes by energy commodity (coal, LNG, crude, renewables)

## Visual Style Variations
- **Classic tornado** — bars sorted by total span (widest at top), used for sensitivity analysis
- **Butterfly chart** — equal category order on both sides for demographic or survey comparison
- **Color-diverging** — red on one side, green on the other to encode positive/negative valence
- **Stacked tornado** — each side has stacked segments for additional breakdown

## Related Charts
- [[Bar Chart]] — one-sided version; simpler but cannot show paired comparison
- [[Dumbbell Chart]] — shows the gap between two points per category on a shared axis
- [[Stacked Bar Chart]] — shows composition within bars but not mirrored comparison
- [[Population Pyramid]] — specific application of the tornado layout for demographic data

## Tools That Support This
- **Infogram** — built-in tornado/butterfly chart type
- **Excel** — achievable with negative-value bar trick on horizontal axis
- **Tableau** — diverging bar chart via calculated fields

## Inspiration Sources
- [Infogram Butterfly Chart Guide](https://infogram.com/blog/butterfly-chart/) — examples and design guidance
- [Tableau Sensitivity Tornado](https://www.tableau.com/blog) — tornado chart for financial modeling
