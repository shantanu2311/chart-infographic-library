---
title: Sankey Diagram
aliases:
  - Flow Diagram
  - Energy Flow Diagram
chart_type: sankey-diagram
category: flow
data_types:
  - categorical
  - continuous
  - hierarchical
  - sequential
data_contexts:
  - Energy Markets
  - Climate & Emissions
  - Public Finance & MDBs
  - Carbon Markets
  - Ember Global Electricity Data
complexity: complex
audience:
  - technical
  - policymaker
  - executive
visual_styles:
  - corporate
  - editorial
  - dashboard
color_approach: categorical
libraries:
  - d3
  - plotly
  - echarts
  - highcharts
  - flourish
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/flow
  - data-type/categorical
  - data-type/quantitative
  - data-type/hierarchical
  - complexity/advanced
  - audience/analyst
  - audience/policymaker
  - audience/researcher
  - theme/energy-markets
  - theme/climate
  - theme/finance
  - theme/carbon-markets
  - theme/iea
  - theme/mdb
  - theme/public-finance
---

# Sankey Diagram

## What It Is
A Sankey diagram is a flow visualization where the width of each link (arrow or band) is proportional to the quantity it represents. Nodes represent categories or stages, and the weighted connections between them show how quantities split, merge, or transfer across a system. They are particularly powerful for revealing where the largest flows concentrate and where losses or inefficiencies occur.

## Best Data Types
- Categorical flows with associated quantities (e.g., energy in petajoules, money in USD, emissions in tCO2e)
- Source-to-destination mappings with magnitude
- Multi-stage transformation or allocation data
- Hierarchical breakdowns where totals must be preserved across stages

## When to Use
- Visualizing how a total quantity distributes across multiple stages or categories
- Showing energy balances (primary supply through transformation to final consumption)
- Mapping financial flows from sources through intermediaries to end recipients
- Tracking material or resource flows through a supply chain
- Communicating system-level views where proportionality matters

## When NOT to Use
> [!warning] Avoid When
> - You have fewer than three nodes or two stages — a simple bar chart will be clearer
> - The flow relationships are bidirectional and roughly symmetric — consider a [[Chord Diagram]] instead
> - Time progression is the primary dimension — an [[Alluvial Diagram]] or [[Line Chart]] is more appropriate
> - The audience is non-technical and unfamiliar with flow diagrams
> - You have too many small flows that create visual clutter (more than ~20 links becomes hard to read)

## Real-World Use Cases
- National energy balance visualizations (e.g., LLNL energy flow charts for the US)
- Government budget allocation from revenue sources to spending departments
- Website user journey mapping from entry to conversion or exit
- Manufacturing process yield analysis showing raw material to product and waste streams

### Energy & Climate Applications
- **IEA World Energy Balance**: Primary energy sources (coal, oil, gas, nuclear, renewables) flowing through transformation (power plants, refineries) to end-use sectors (industry, transport, buildings, agriculture)
- **GHG Scope 1/2/3 Emission Flows**: Mapping a company's or country's emission sources through scope classification to specific categories (stationary combustion, purchased electricity, upstream transport, etc.)
- **Climate Finance Flows**: Tracking capital from sources (MDBs, bilateral agencies, private sector) through intermediaries (green climate fund, national development banks) to recipient countries or projects
- **Carbon Credit Flows**: Visualizing credit movement from registries (Verra, Gold Standard) through brokers and exchanges to end buyers and retirement
- **Critical Mineral Supply Chains**: Showing extraction countries flowing through refining nations to manufacturing hubs for batteries, solar panels, and wind turbines

## Visual Style Variations
- **Horizontal flow** (most common): nodes arranged left to right with curved links
- **Vertical flow**: top-to-bottom arrangement, useful for hierarchical breakdowns
- **Color-coded by source**: each origin node's color carries through its downstream links
- **Color-coded by destination**: links take the color of the receiving node, emphasizing where flows end up
- **Interactive/hover**: digital implementations where hovering highlights a single flow path

## Related Charts
- [[Alluvial Diagram]] — similar flow structure but specifically designed for categorical changes across discrete time stages
- [[Chord Diagram]] — better suited when flows are bidirectional and you want to show the full matrix of inter-relationships
- [[Funnel Chart]] — appropriate when the flow is strictly sequential with monotonically decreasing values at each stage

## Inspiration Sources
- [IEA World Energy Balances](https://www.iea.org/data-and-statistics/data-tools/energy-statistics-data-browser) — the canonical energy Sankey showing global primary energy to end use
- [LLNL Energy Flow Charts](https://flowcharts.llnl.gov/) — Lawrence Livermore National Laboratory's annual US energy and carbon flow diagrams
- [Climate Policy Initiative Global Landscape of Climate Finance](https://www.climatepolicyinitiative.org/publication/global-landscape-of-climate-finance-2023/) — tracks climate finance flows from source to use
- [Our World in Data Energy Mix](https://ourworldindata.org/energy-mix) — energy data that can be restructured as Sankey flows
