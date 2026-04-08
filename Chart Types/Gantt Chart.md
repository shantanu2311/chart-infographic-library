---
title: Gantt Chart
aliases:
  - Timeline Chart
  - Project Timeline
  - Schedule Chart
  - Bar Schedule
tags:
  - chart-type/temporal
  - data-type/duration
  - data-type/categorical
  - data-type/sequential
  - complexity/intermediate
  - audience/project-managers
  - audience/policymakers
  - audience/executives
  - audience/investors
  - theme/energy
  - theme/climate
  - theme/finance
  - theme/net-zero
  - theme/infrastructure
category: Temporal
complexity: intermediate
best_audience: project managers, policymakers, executives, investors
---

# Gantt Chart

## What It Is
A Gantt chart represents tasks, phases, or events as horizontal bars along a time axis, with each bar's left edge marking the start date and its length encoding duration. Dependencies between tasks can be shown with arrows or connector lines. Originally developed for industrial production scheduling, the Gantt chart has become the standard visualization for project timelines, policy implementation roadmaps, and any scenario where overlapping durations and sequencing need to be communicated at a glance.

## Best Data Types
- Tasks or activities with defined start and end dates
- Project phases with sequential or parallel relationships
- Milestones (zero-duration markers) on a timeline
- Hierarchical work breakdown structures with parent and child tasks
- Resource allocation schedules showing who or what is engaged over time

## When to Use
- Planning and communicating project schedules with multiple parallel workstreams
- Showing the critical path and dependencies between sequential phases
- Tracking progress against planned timelines with percent-complete overlays
- Presenting policy or strategy implementation roadmaps to stakeholders
- Comparing planned versus actual timelines for retrospective analysis

## When NOT to Use
> [!warning] Avoid When
> - You have hundreds of tasks at the same detail level; the chart becomes an unreadable wall of bars (aggregate into phases first)
> - The focus is on trends or magnitudes over time rather than durations (use a [[Line Chart]] or [[Area Chart]])
> - Tasks have no meaningful time dimension (use a [[Kanban Board]] or simple checklist)
> - You need to show cumulative or stacked quantities over time (use a [[Waterfall Chart]] or [[Stacked Area Chart]])
> - The audience needs to compare values rather than durations; bar length on a time axis does not invite magnitude comparison

## Real-World Use Cases
- Software development sprint planning with feature tasks and dependencies
- Construction project scheduling across design, permitting, and build phases
- Event planning timelines with vendor coordination milestones
- Academic research project timelines from proposal to publication

### Energy & Climate Applications
- Renewable energy project development timeline from feasibility study through permitting, procurement, construction, and commissioning (typical 18-36 month cycle for utility-scale solar)
- MDB project cycle milestones mapping the World Bank or ADB pipeline from concept note through board approval, disbursement, and completion review
- COP/UNFCCC negotiation schedule showing intersessional meetings, technical dialogues, Global Stocktake phases, and ministerial segments across a two-year cycle
- National energy transition roadmap milestones (e.g., India's targets: 500 GW non-fossil by 2030, net zero by 2070) with interim policy and infrastructure deadlines
- NDC implementation timeline tracking legislative, regulatory, and investment actions required to meet Nationally Determined Contribution targets
- Critical mineral supply chain development phases from exploration through mine development, refinery construction, and first production

## Visual Style Variations
- **Basic bar timeline** with colored horizontal bars grouped by workstream or category
- **Dependency-linked Gantt** with arrows showing finish-to-start, start-to-start, or other task relationships
- **Progress-overlay Gantt** showing percent complete as a filled portion within each bar, often with a vertical "today" line
- **Milestone-annotated timeline** combining duration bars with diamond or circle markers for key decision points and deadlines

## Related Charts
- [[Line Chart]] — better for showing continuous trends over the same time period
- [[Waterfall Chart]] — shows cumulative build-up or breakdown of a total, sometimes used alongside Gantt for cost or emission reduction sequencing
- [[Bump Chart]] — tracks rank changes over time periods rather than task durations
- [[Timeline]] — simplified version focusing on discrete events rather than duration bars
- [[Swimlane Diagram]] — similar horizontal layout but organized by actor or department rather than time dependency

## Inspiration Sources
- [IEA Net Zero Roadmap](https://www.iea.org/reports/net-zero-by-2050) — milestone-style Gantt timelines for sector decarbonization pathways to 2050
- [IRENA Project Development Guides](https://www.irena.org/) — renewable energy project lifecycle timelines from resource assessment to grid connection
- [World Bank Project Cycle](https://www.worldbank.org/en/projects-operations/products-and-services/brief/projectcycle) — canonical MDB project phase diagram adaptable as a Gantt chart
- [Mermaid.js Gantt Syntax](https://mermaid.js.org/syntax/gantt.html) — lightweight text-based Gantt chart generation for documentation and markdown environments
