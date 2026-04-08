---
title: Hierarchical Infographic
tags:
  - infographic-style
  - hierarchy
  - taxonomy
  - ghg-scopes
  - eu-taxonomy
  - organizational-structure
---

# Hierarchical Infographic

## What It Is
An infographic format that visualizes nested structures, taxonomies, and parent-child relationships through layered, branching, or containment-based layouts. It reveals how complex systems decompose into sub-components, how categories nest within broader classifications, and how authority or information flows through organizational layers. This format makes invisible structures visible and is critical for governance, reporting frameworks, and supply chain analysis.

## Key Characteristics
- Clear parent-child visual relationships through nesting, branching, or containment
- Progressive disclosure from broad categories to granular detail
- Consistent visual encoding of hierarchy depth (size, color saturation, indentation)
- Proportional sizing where node area reflects magnitude (emissions, budget, headcount)
- Drill-down capability in digital formats, expanding nodes on click or hover

## Best Use Cases
- GHG inventory decomposition: Total emissions > Scope 1/2/3 > Category > Source > Fuel type
- EU Taxonomy classification: Objective > Sector > Activity > Technical screening criteria
- UNFCCC reporting structure: National Communication > Biennial Report > sectoral chapters
- Energy supply chain hierarchy: primary energy > conversion > transmission > distribution > end use
- MDB organizational structure: Board > Vice Presidencies > Global Practices > Country Offices

### Energy & Climate Applications
- Scope 1/2/3 emissions breakdown for a steel facility down to individual source level
- TCFD disclosure framework: Governance > Strategy > Risk Management > Metrics & Targets
- Critical mineral supply chain: ore extraction > refining > component manufacturing > assembly > recycling
- Climate finance architecture: multilateral funds > implementing entities > executing agencies > project level
- Indian MSME sector taxonomy: sector > sub-sector > process type > emission sources

## Structure & Layout
The most common layouts are top-down tree diagrams, concentric ring diagrams (sunburst), and area-proportional rectangles (treemap). Tree diagrams work best when the hierarchy has 2-4 levels and fewer than 30 terminal nodes. Treemaps excel when proportional sizing matters and space is constrained. Sunbursts are ideal for showing part-to-whole relationships within each level simultaneously. The root node sits at the top (tree), center (sunburst), or occupies the full canvas (treemap). Labels are placed within nodes for treemaps, along radial spokes for sunbursts, and beside nodes for trees. Color encodes either the top-level category (consistent hue per branch) or a secondary variable like growth rate or data quality score.

## Design Tips
> [!tip] Best Practices
> - Limit visible depth to 3-4 levels in static formats; use interactivity for deeper hierarchies
> - Apply color by top-level branch, then use saturation variation for sub-levels within each branch
> - Size nodes proportionally to their quantitative value — avoid equal-sized nodes when magnitudes differ significantly
> - Provide a breadcrumb trail or zoom-out control in interactive versions so users maintain orientation
> - Label leaf nodes only when they exceed a minimum size threshold (e.g., >3% of total) to prevent text overlap

## When NOT to Use
> [!warning] Avoid When
> - Relationships are primarily lateral (peer-to-peer networks) rather than hierarchical
> - The hierarchy has more than 5 levels with hundreds of leaf nodes in a static format (use interactive or tabular drill-down)
> - The audience cares about trends over time rather than structural decomposition

## Recommended Chart Types
- [[Treemap]] — area-proportional rectangles showing nested part-to-whole at every level simultaneously
- [[Sunburst Chart]] — concentric rings revealing hierarchy from center outward with angular proportionality
- [[Network Diagram]] — node-link visualization for hierarchies with cross-cutting connections or shared sub-components

## Inspiration Sources
- [GHG Protocol Scope 3 Calculation Guidance](https://ghgprotocol.org/scope-3-calculation-guidance) — category decomposition visuals
- [EU Taxonomy Compass](https://ec.europa.eu/sustainable-finance-taxonomy/) — interactive classification explorer
- [IEA World Energy Balances](https://www.iea.org/data-and-statistics/data-tools/world-energy-balances) — energy flow decomposition from primary to end use
