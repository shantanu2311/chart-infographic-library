---
title: Sunburst Chart
aliases:
  - Sunburst Diagram
  - Multi-level Pie Chart
  - Radial Treemap
tags:
  - chart-type/composition
  - data-type/hierarchical
  - data-type/multi-level
  - complexity/advanced
  - audience/analysts
  - audience/researchers
  - audience/technical
  - theme/emissions
  - theme/supply-chain
  - theme/UNFCCC
  - theme/GHG-protocol
category: Composition
complexity: advanced
best_audience: analysts, researchers, technical audiences
---

# Sunburst Chart

## What It Is
A sunburst chart is a radial, multi-ring visualization that represents hierarchical data. The innermost ring shows the top-level categories, and each successive ring represents a deeper level in the hierarchy. Segment arc length is proportional to a quantitative value. It combines the part-of-whole logic of a [[Donut Chart]] with the hierarchical depth of a [[Treemap]], making it particularly effective for tracing paths from root to leaf through nested categories.

## Best Data Types
- Multi-level hierarchical data (2-4 levels deep)
- Nested categorical taxonomies with associated quantities
- Data where the path from root to leaf is meaningful (e.g., Scope > Category > Source)
- Organizational or classification structures with quantitative weights

## When to Use
- Showing how a total decomposes through multiple levels of a hierarchy simultaneously
- Tracing the contribution path from a top-level category down to individual items
- Exploring taxonomies or classification systems interactively
- When the radial layout makes better use of available space than a nested treemap
- Communicating the structure of reporting frameworks (GHG Protocol, UNFCCC categories)

## When NOT to Use
> [!warning] Avoid When
> - The hierarchy has more than 4 levels (outer rings become unreadably thin)
> - You need precise quantitative comparisons (arc lengths are harder to compare than bar lengths)
> - The dataset has very unequal branch sizes, causing some segments to be too small
> - The audience is non-technical and unfamiliar with radial hierarchical charts
> - A simple [[Donut Chart]] or [[Treemap]] would convey the same message more clearly

## Real-World Use Cases
- File system visualization: root > folders > subfolders > files
- Organizational charts: company > division > department > team
- Biological taxonomy: kingdom > phylum > class > order
- Website navigation structure: domain > section > page > component

### Energy & Climate Applications
- GHG inventory breakdown: Scope (1/2/3) > Category (stationary combustion, purchased electricity, etc.) > Source (natural gas, grid power, diesel)
- Energy supply chain mapping: extraction > processing > refining > distribution > end use
- UNFCCC reporting taxonomy: sector > sub-sector > gas type, visualizing national inventory structure
- Carbon footprint decomposition: organization > facility > process > emission source
- Climate finance flows: source (bilateral/multilateral) > instrument (grant/loan/equity) > theme (mitigation/adaptation)

## Visual Style Variations
- **Standard sunburst** — concentric rings with color-coded segments and hover tooltips
- **Interactive drill-down** — click a segment to zoom in and make it the new center
- **Partial sunburst** — semi-circular variant for dashboard integration
- **Gradient-encoded** — color intensity on the outermost ring encodes a second variable (e.g., data quality score)

## Related Charts
- [[Treemap]] — rectangular alternative for hierarchical data; better for precise area comparison
- [[Donut Chart]] — single-ring version; use when only one level of hierarchy is needed
- [[Chord Diagram]] — shows relationships between categories rather than hierarchical decomposition

## Inspiration Sources
- [GHG Protocol Scope 3 Guidance](https://ghgprotocol.org/scope-3-guidance) — multi-level emission category breakdowns
- [UNFCCC National Inventory Submissions](https://unfccc.int/ghg-inventories-annex-i-parties) — hierarchical reporting taxonomy
- [D3.js Sunburst Examples](https://observablehq.com/@d3/sunburst) — interactive radial hierarchy visualizations
