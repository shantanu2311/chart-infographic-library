---
title: Network Diagram
aliases:
  - Graph
  - Node-Link Diagram
  - Network Graph
  - Force-Directed Graph
chart_type: network-diagram
category: relationship
data_types:
  - relational
  - categorical
data_contexts:
  - Supply Chain & Critical Minerals
  - Geopolitics & Energy Security
  - Carbon Markets
complexity: complex
audience:
  - technical
  - academic
visual_styles:
  - editorial
  - artistic
  - dashboard
color_approach: categorical
libraries:
  - d3
  - plotly
  - echarts
  - flourish
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/relationship
  - data-type/relational
  - data-type/connections
  - data-type/graph
  - complexity/advanced
  - audience/analysts
  - audience/researchers
  - audience/policy-makers
  - theme/energy-markets
  - theme/supply-chain
  - theme/critical-minerals
  - theme/climate-finance
  - theme/COP-UNFCCC
---

# Network Diagram

## What It Is
A network diagram (or graph visualization) represents entities as nodes and relationships between them as edges (links). Nodes can be sized, colored, or shaped to encode attributes, while edges can vary in thickness, color, or style to represent relationship strength, direction, or type. Network diagrams are the primary tool for understanding complex relational structures — who is connected to whom, how densely, and through what pathways.

## Best Data Types
- Relational data: pairs of entities with connections (edges)
- Graph data: nodes with attributes and edges with weights or types
- Flow data: directed connections showing movement or influence
- Membership and affiliation data: entities belonging to groups or networks
- Supply chain and trade data: bilateral flows between entities

## When to Use
- Mapping relationships and dependencies between entities (countries, companies, technologies)
- Identifying central nodes (hubs), bridges, and isolated clusters in a system
- Visualizing trade flows, ownership structures, or influence pathways
- Understanding supply chain vulnerabilities and dependencies
- Exploring how information, materials, or money flows through a network

## When NOT to Use
> [!warning] Avoid When
> - The network has more than 200-300 nodes without interactive filtering (visual clutter makes it unreadable)
> - The relationships are purely quantitative and have no structural meaning (use a [[Heatmap]] or [[Correlogram]])
> - A simpler hierarchical structure exists (use a [[Treemap]] or [[Sunburst Chart]])
> - The audience needs precise quantitative comparisons (node positions in force layouts are not meaningful axes)
> - Directed flow volumes are the primary message (use a [[Sankey Diagram]] or [[Chord Diagram]] instead)

## Real-World Use Cases
- Social media: follower/following networks, community detection
- IT infrastructure: server dependencies, microservice communication maps
- Academic research: citation networks, co-authorship graphs
- Law enforcement: criminal network analysis, money laundering trails

### Energy & Climate Applications
- International energy trade networks: oil, gas, LNG, and electricity bilateral flows between countries
- Corporate ownership structures in the fossil fuel industry: parent companies, subsidiaries, joint ventures
- Critical mineral supply chain dependencies: mining countries > processing countries > manufacturing countries > end-use markets
- Climate policy influence networks: mapping how UNFCCC negotiating blocs, NGOs, and industry groups interact at COP summits
- Grid interconnection maps: electricity transmission links between regions and countries with capacity and utilization

## Visual Style Variations
- **Force-directed layout** — nodes repel each other, edges act as springs; reveals organic cluster structure
- **Hierarchical / tree layout** — nodes arranged in levels, showing directed acyclic graphs (DAGs)
- **Circular layout** — nodes placed around a circle, edges drawn as chords or arcs inside
- **Geographic network** — nodes positioned on a map at their real-world locations, edges as lines or arcs between them

## Related Charts
- [[Chord Diagram]] — circular visualization of flows between categories; better for showing mutual relationships within a closed set
- [[Sankey Diagram]] — flow-based diagram emphasizing volume through a system; better for directional flow quantities
- [[Arc Diagram]] — one-dimensional layout where nodes are on a line and edges are arcs; simpler but less expressive

## Inspiration Sources
- [UN Comtrade Database](https://comtradeplus.un.org/) — bilateral trade data for constructing energy trade networks
- [Global Energy Monitor](https://globalenergymonitor.org/) — fossil fuel project ownership and infrastructure data
- [IEA Critical Minerals Report](https://www.iea.org/reports/the-role-of-critical-minerals-in-clean-energy-transitions) — supply chain dependency mapping
