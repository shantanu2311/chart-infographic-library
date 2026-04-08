---
title: Bullet Chart
aliases:
  - Bullet Graph
tags:
  - chart-type/comparison
  - data-type/actual-vs-target
  - data-type/numeric
  - complexity/intermediate
  - audience/executive
  - audience/analyst
  - theme/net-zero
  - theme/cop-unfccc
  - theme/mdb
  - theme/renewable-energy
  - theme/climate
  - theme/public-finance
category: Comparison
complexity: intermediate
best_audience: executive, analyst
---

# Bullet Chart

## What It Is
A bullet chart, designed by Stephen Few as a replacement for dashboard gauges, displays a primary measure (a bar), compares it against a target (a marker line), and places both within qualitative ranges (shaded background bands representing poor, satisfactory, and good performance). It packs a dense amount of information into a compact horizontal space, making it ideal for KPI dashboards and performance tracking.

## Best Data Types
- A single quantitative measure with a defined target or benchmark
- Actual vs planned/budgeted/committed values
- Performance metrics with qualitative thresholds (poor, acceptable, good, excellent)
- KPIs that need context beyond a simple number
- Progress tracking against goals or commitments

## When to Use
- Tracking progress against a defined target (NDC commitments, budget utilisation)
- Dashboard displays where space is limited and multiple KPIs must be shown
- Replacing pie charts or gauges that waste space and lack precision
- When you need to communicate actual performance, target, and qualitative context simultaneously
- Executive reporting where quick red/amber/green assessment is needed

## When NOT to Use
> [!warning] Avoid When
> - The audience is unfamiliar with bullet charts (they require brief explanation on first use)
> - You have no target or benchmark to compare against (use a simple [[Bar Chart]])
> - You need to show trends over time (bullet charts are point-in-time snapshots)
> - You want to compare many categories against each other rather than against individual targets
> - The qualitative ranges are arbitrary or poorly defined, which would mislead rather than inform

## Real-World Use Cases
- Sales quota attainment by sales representative
- Project budget spent vs allocated across departments
- Manufacturing output vs production target
- Hospital bed occupancy vs capacity threshold

### Energy & Climate Applications
- NDC target vs actual emissions reduction progress for each G20 country (UNFCCC Global Stocktake data)
- Renewable capacity target vs installed capacity (e.g., India's 500 GW by 2030 target vs current ~200 GW)
- MDB climate finance commitment vs actual disbursement (World Bank, GCF, CIF annual reports)
- Corporate net-zero interim targets vs reported Scope 1+2 emissions (CDP/SBTi data)
- National energy efficiency improvement target vs realised savings (BEE PAT cycle data)

## Visual Style Variations
- **Horizontal bullet** — the standard orientation; multiple bullets stacked vertically for a KPI dashboard
- **Vertical bullet** — rotated 90 degrees; useful when comparing few items side by side
- **Colour-coded ranges** — traffic-light shading (red/amber/green) for qualitative bands instead of grey gradients
- **Multi-measure bullet** — two bars (e.g., current year and previous year) against the same target for trend context

## Related Charts
- [[Bar Chart]] — simpler alternative when no target or qualitative context is needed
- [[Dumbbell Chart]] — shows the gap between two values per category without qualitative ranges
- [[Waterfall Chart]] — breaks down how components contribute to reaching (or missing) a target
- [[Lollipop Chart]] — lighter visual for ranked single-measure comparisons

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Stephen Few — Bullet Graph Design Specification](https://www.perceptualedge.com/articles/misc/Bullet_Graph_Design_Spec.pdf) — the original specification
- [Climate Action Tracker](https://climateactiontracker.org/) — target vs actual tracking for national climate policies
