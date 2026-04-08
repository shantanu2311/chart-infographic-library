---
title: Chord Diagram
aliases:
  - Chord Graph
  - Radial Network Diagram
tags:
  - chart-type/flow
  - data-type/relational
  - data-type/matrix
  - data-type/bidirectional
  - complexity/advanced
  - audience/analyst
  - audience/researcher
  - theme/energy-markets
  - theme/climate
  - theme/finance
  - theme/critical-minerals
  - theme/carbon-markets
  - theme/supply-chain
category: Flow
complexity: advanced
best_audience: analysts, researchers, data scientists
---

# Chord Diagram

## What It Is
A chord diagram arranges entities around a circle and draws arcs (chords) between them, where the thickness of each chord represents the magnitude of the relationship or flow between the connected entities. It excels at showing the full matrix of bilateral relationships in a compact, visually striking layout. The arc length each entity occupies on the circle's perimeter indicates its total flow volume.

## Best Data Types
- Square matrices of bilateral flows (exports/imports, transfers, trades)
- Co-occurrence or correlation matrices
- Bidirectional relationship data where both directions matter
- Network data with weighted edges between a moderate number of nodes

## When to Use
- Showing inter-entity trade or transfer flows where bidirectional relationships matter
- Visualizing which pairs have the strongest connections in a network
- Displaying a full origin-destination matrix in a single compact view
- Communicating the relative importance of each entity (via its arc length) alongside its relationships

## When NOT to Use
> [!warning] Avoid When
> - The flow is strictly unidirectional or hierarchical — use a [[Sankey Diagram]] instead
> - You have more than ~15 entities — the diagram becomes an unreadable tangle of chords
> - Precise values matter more than patterns — a heatmap or table is more readable
> - The audience is unfamiliar with circular layouts — the learning curve is steep
> - Relationships are unweighted (just connected or not) — a simpler network diagram works better

## Real-World Use Cases
- International merchandise trade flows between major economies
- Migration flows between countries or regions
- Citation networks between academic journals
- Inter-departmental collaboration or communication patterns in organizations

### Energy & Climate Applications
- **Inter-Country Energy Trade Flows**: Oil, gas, LNG, and electricity trade volumes between major trading nations (e.g., Middle East to Asia, Russia to Europe, US to Mexico)
- **Cross-Sector Emission Linkages**: How emissions in one sector (power generation) create indirect emissions in others (industry, buildings, transport) through electricity and heat consumption
- **Bilateral Climate Finance Flows**: Donor-to-recipient country climate finance transfers, showing which developed nations fund which developing nations and in what volumes
- **Critical Mineral Trade Relationships**: Extraction-to-refining-to-manufacturing trade flows for lithium, cobalt, nickel, and rare earths between countries like DRC, Australia, Chile, China, Japan, South Korea, and the US
- **Carbon Credit Cross-Border Flows**: Voluntary and compliance carbon credit transfers between registries, countries, and market participants under Article 6 mechanisms

## Visual Style Variations
- **Full matrix**: all chords shown simultaneously with color coding by source entity
- **Interactive highlight**: hovering on one entity dims all others, isolating its specific relationships
- **Directional chords**: asymmetric chord widths at each end to show net flow direction
- **Grouped chords**: entities clustered by region or category with gaps between groups for visual separation

## Related Charts
- [[Sankey Diagram]] — better for unidirectional multi-stage flows where hierarchy matters
- [[Network Diagram]] — more flexible layout for complex networks with many nodes, but loses the proportional arc representation
- [[Arc Diagram]] — a linearized version where nodes are on a line and arcs connect them, simpler but less compact

## Inspiration Sources
- [UN Comtrade Database](https://comtradeplus.un.org/) — bilateral trade data ideal for energy commodity chord diagrams
- [IEA World Energy Outlook Trade Flows](https://www.iea.org/reports/world-energy-outlook-2023) — inter-regional energy trade projections
- [OECD Climate Finance Data](https://www.oecd.org/en/topics/climate-finance.html) — bilateral climate finance flows between donor and recipient countries
- [MIT Observatory of Economic Complexity](https://oec.world/) — interactive trade flow visualizations for energy commodities and minerals
