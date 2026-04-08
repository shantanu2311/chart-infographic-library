---
title: Packed Circle Chart
aliases:
  - Circle Packing
tags:
  - chart-type/hierarchical
  - data-type/hierarchical
  - data-type/categorical
  - data-type/quantitative
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/researcher
  - theme/energy
  - theme/climate
  - theme/mdb
  - theme/supply-chain
category: Hierarchical
complexity: intermediate
best_audience: analysts, researchers, executives
---

# Packed Circle Chart

## What It Is
A packed circle chart (circle packing) represents hierarchical data using nested circles, where each circle's area is proportional to a quantitative value. Parent categories contain their children, creating a visual nesting that communicates both the hierarchy and relative magnitude simultaneously. The organic, bubble-like aesthetic makes it visually engaging while encoding two dimensions: structure and size.

## Best Data Types
- Hierarchical or tree-structured data (2-4 levels deep)
- Categorical data with nested sub-categories and a size metric
- Portfolio breakdowns with sector/sub-sector/project nesting
- Organizational or taxonomic classifications with quantitative weights

## When to Use
- Showing part-to-whole relationships within a hierarchy (e.g., global emissions by sector > sub-sector)
- Visualizing portfolio composition across multiple levels
- When the organic layout is more engaging than rectangular [[Treemap]] grids
- Comparing relative sizes across and within groups
- When you want to emphasize that small items exist even if their area is tiny

## When NOT to Use
> [!warning] Avoid When
> - Precise value comparison is required (circles are harder to compare than rectangles)
> - The hierarchy has more than 4 levels (becomes visually cluttered)
> - You have very few categories (a simple [[Bar Chart]] or [[Donut Chart]] is clearer)
> - Data is not hierarchical (use [[Bubble Chart]] for flat data with size encoding)
> - Exact proportions matter more than visual impression

## Real-World Use Cases
- Software dependency visualization (package sizes nested in modules)
- News topic clustering by volume of coverage
- Government budget breakdowns by department and program
- Species biodiversity by kingdom, phylum, class

### Energy & Climate Applications
- GHG emissions by sector > sub-sector as nested circles (energy > electricity > coal/gas/oil)
- MDB climate portfolio by theme > project (mitigation > renewable > solar/wind/hydro)
- Global energy production by region > country, circle area proportional to TWh
- Carbon credit issuance by standard > methodology > project type
- Supply chain Scope 3 emissions by category > supplier tier

## Visual Style Variations
- **Flat packing** — single-level circles packed without nesting, sized by value
- **Nested hierarchy** — 2-3 levels of containment with color coding per level
- **Zoomable packing** — interactive drill-down from top-level to leaf nodes
- **Labeled packing** — text labels inside circles, sized to fit available space

## Related Charts
- [[Treemap]] — rectangular alternative; better for precise area comparison but less visually organic
- [[Sunburst Chart]] — radial hierarchy; better for showing path from root to leaf
- [[Bubble Chart]] — flat (non-nested) circles on x/y axes; for relationships not hierarchies

## Tools That Support This
- **D3.js** — `d3.pack()` layout with full customization
- **Flourish** — built-in circle packing template with animation
- **Canva** — simplified circle packing in infographic templates

## Inspiration Sources
- [D3 Circle Packing Gallery](https://observablehq.com/@d3/circle-packing) — interactive examples with code
- [Flourish Templates](https://flourish.studio/visualisations/hierarchy/) — hierarchy visualization templates
