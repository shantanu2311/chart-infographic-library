---
title: Funnel Chart
aliases:
  - Pipeline Chart
  - Conversion Funnel
tags:
  - chart-type/flow
  - data-type/sequential
  - data-type/categorical
  - data-type/quantitative
  - complexity/intermediate
  - audience/executive
  - audience/analyst
  - audience/policymaker
  - theme/finance
  - theme/mdb
  - theme/carbon-markets
  - theme/renewable-energy
  - theme/public-finance
category: Flow
complexity: intermediate
best_audience: executives, analysts, policymakers, project managers
---

# Funnel Chart

## What It Is
A funnel chart displays values across sequential stages of a process, typically narrowing from top to bottom to reflect decreasing quantities at each step. Each horizontal bar or trapezoid represents a stage, and its width (or area) is proportional to the value at that stage. Funnels are intuitive for showing attrition, conversion rates, or pipeline progression where drop-off between stages is the key insight.

## Best Data Types
- Sequential process stages with decreasing (or occasionally increasing) quantities
- Conversion or attrition data across defined pipeline steps
- Project lifecycle counts at each phase
- Any data where the narrative is about progressive filtering or loss

## When to Use
- Showing how many items survive each stage of a multi-step process
- Visualizing project pipelines from identification to completion
- Communicating drop-off rates between stages to highlight bottlenecks
- Presenting sales or approval funnels where stakeholders care about conversion efficiency

## When NOT to Use
> [!warning] Avoid When
> - Values do not follow a generally sequential or decreasing pattern — a [[Bar Chart]] is more honest
> - You need to show the composition within each stage — use a [[Stacked Bar Chart]]
> - The stages have complex branching or feedback loops — a [[Sankey Diagram]] captures this better
> - You need to show changes over time — the funnel is a snapshot, not a time series
> - There are only two stages — a simple comparison (bar or number pair) is sufficient

## Real-World Use Cases
- Sales pipeline visualization (leads to qualified to proposal to closed-won)
- Recruitment funnel (applications to interviews to offers to hires)
- E-commerce conversion (visitors to cart to checkout to purchase)
- Clinical trial phases (screened to enrolled to completed to analyzed)

### Energy & Climate Applications
- **Renewable Energy Project Pipeline**: Projects identified > pre-feasibility > feasibility > approved > financial close > under construction > operational, showing where projects stall or drop out
- **Carbon Credit Lifecycle**: Credits issued > listed on exchange > transacted > transferred > retired, revealing market liquidity and retirement rates
- **MDB Project Cycle**: Concept note > appraisal > board approval > first disbursement > completion > evaluation, highlighting approval bottlenecks
- **Green Bond Issuance Pipeline**: Mandated > structured > marketed > priced > allocated > listed, showing deal attrition
- **CDM/Article 6 Project Registration**: PIN submitted > validation > registration > monitoring > verification > CER issuance, revealing regulatory bottlenecks

## Visual Style Variations
- **Symmetric funnel**: centered trapezoids narrowing evenly from both sides (classic style)
- **Left-aligned bars**: horizontal bars of decreasing length, easier to read precise values
- **Percentage-annotated**: each stage shows both absolute count and percentage of the initial stage
- **Color-gradient**: stages transition from one color to another (e.g., green to red) to encode performance

## Related Charts
- [[Waterfall Chart]] — shows incremental positive and negative changes leading to a final total, complementary to the funnel's attrition view
- [[Bar Chart]] — simpler alternative when the sequential nature is not the primary message
- [[Sankey Diagram]] — better when the flow branches or merges rather than strictly narrowing

## Inspiration Sources
- [Global CCS Institute Project Database](https://www.globalccsinstitute.com/resources/co2re/) — CCS project pipeline data across development stages
- [BloombergNEF Renewable Energy Project Database](https://about.bnef.com/) — project pipeline from development to operational
- [World Bank Project Cycle](https://projects.worldbank.org/) — MDB project lifecycle stages with public data
- [Verra Registry Dashboard](https://registry.verra.org/) — carbon credit issuance and retirement pipeline data
