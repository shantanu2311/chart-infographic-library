---
title: Waterfall Chart
aliases:
  - Bridge Chart
  - Walk Chart
  - Cascade Chart
chart_type: waterfall-chart
category: specialized
data_types:
  - categorical
  - continuous
  - sequential
data_contexts:
  - Climate & Emissions
  - Renewable Energy & Transition
  - Financial Markets
  - Public Finance & MDBs
complexity: medium
audience:
  - executive
  - technical
  - policymaker
visual_styles:
  - corporate
  - minimal
  - editorial
color_approach: diverging
libraries:
  - d3
  - plotly
  - echarts
  - recharts
  - highcharts
  - flourish
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/specialized
  - data-type/quantitative
  - data-type/sequential
  - data-type/incremental
  - complexity/intermediate
  - audience/executive
  - audience/analyst
  - audience/policymaker
  - theme/climate
  - theme/energy-markets
  - theme/finance
  - theme/renewable-energy
  - theme/net-zero
  - theme/public-finance
---

# Waterfall Chart

## What It Is
A waterfall chart shows how an initial value is affected by a series of intermediate positive and negative contributions to arrive at a final value. Each bar "floats" above or hangs below its predecessor, with color coding distinguishing increases (typically green) from decreases (typically red) and totals (typically blue or grey). The visual stepping pattern explains the "bridge" between two states, making it one of the most effective charts for decomposing change.

## Best Data Types
- A starting value, a series of positive and negative incremental changes, and a resulting total
- Variance analysis data (budget vs. actual, year-over-year change drivers)
- Cost or revenue buildup from individual components
- Any sequential additive/subtractive breakdown leading to a net result

## When to Use
- Explaining how a total changed from one period to another through contributing factors
- Breaking down the components of a cost, price, or emission total
- Presenting variance analysis (what drove the difference between plan and actual)
- Showing a "carbon budget" being consumed by different emission sources
- Communicating financial results where stakeholders need to understand drivers of change

## When NOT to Use
> [!warning] Avoid When
> - The components are not additive (e.g., multiplicative or percentage-based relationships) — the visual logic breaks
> - You have too many intermediate steps (more than ~12) — the chart becomes hard to follow
> - The audience needs to compare multiple waterfall series side by side — small multiples or a grouped bar chart works better
> - The data is a simple time series — use a [[Line Chart]] instead
> - Components can be both positive and negative within the same category — this creates confusion about the bar direction

## Real-World Use Cases
- McKinsey-style profit bridge (revenue + cost changes from Q1 to Q2)
- Government budget reconciliation (planned vs. actual spending drivers)
- Project cost overrun analysis (original budget through change orders to final cost)
- Customer count bridge (opening balance + new - churned = closing balance)

### Energy & Climate Applications
- **GHG Inventory Bridge (Base Year to Current)**: Starting from base year emissions, showing increases (production growth, new facilities) and decreases (efficiency gains, fuel switching, renewable procurement) arriving at current year emissions
- **Cost Buildup of Renewable Projects**: Breaking down LCOE or total project cost into components — equipment, installation, grid connection, financing, O&M, land, permitting — building from zero to total cost per MWh
- **Revenue Waterfall for Energy Companies**: How an energy company's revenue changes from one year to the next through volume effects, price effects, currency effects, and portfolio changes
- **Carbon Budget Remaining Analysis**: Starting from the 1.5C carbon budget, subtracting historical cumulative emissions, committed infrastructure emissions, and projected additions to show the remaining budget
- **LCOE Component Breakdown**: Decomposing the levelized cost of energy into capital cost, cost of capital, capacity factor, O&M, fuel cost, and carbon cost contributions for different technologies

## Visual Style Variations
- **Horizontal (classic)**: bars progress left to right with connector lines between floating bars
- **Color-coded**: green for increases, red for decreases, blue/grey for subtotals and final total
- **Stacked waterfall**: each bar is itself a stacked bar showing sub-components of that step
- **Annotated with percentages**: each step labeled with both absolute value and percentage contribution to the total change

## Related Charts
- [[Stacked Bar Chart]] — shows composition at a single point; the waterfall shows how composition changes between two points
- [[Bar Chart]] — simpler alternative when the additive build-up narrative is not needed
- [[Funnel Chart]] — shows sequential attrition like a waterfall but without the positive/negative distinction

## Inspiration Sources
- [McKinsey Quarterly](https://www.mckinsey.com/quarterly/overview) — the consulting firm that popularized the bridge chart format
- [IEA World Energy Outlook Decomposition Charts](https://www.iea.org/reports/world-energy-outlook-2023) — emission change decomposition by driver
- [Carbon Brief Analysis](https://www.carbonbrief.org/) — carbon budget remaining waterfall visualizations
- [IRENA Renewable Cost Reports](https://www.irena.org/Publications) — LCOE component breakdowns
- [Global Carbon Project Budget](https://www.globalcarbonproject.org/carbonbudget/) — remaining carbon budget decomposition
