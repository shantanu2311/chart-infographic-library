---
title: Alluvial Diagram
aliases:
  - Alluvial Plot
  - Parallel Sets Diagram
tags:
  - chart-type/flow
  - data-type/categorical
  - data-type/temporal
  - data-type/longitudinal
  - complexity/advanced
  - audience/analyst
  - audience/researcher
  - audience/policymaker
  - theme/energy-markets
  - theme/climate
  - theme/carbon-markets
  - theme/cop-unfccc
  - theme/mdb
  - theme/renewable-energy
category: Flow
complexity: advanced
best_audience: analysts, researchers, policymakers
---

# Alluvial Diagram

## What It Is
An alluvial diagram visualizes how categorical compositions change across discrete stages or time periods. Named after alluvial fans in geology, the flowing bands between vertical axes show how items migrate between categories from one stage to the next. Unlike a Sankey diagram which focuses on system-level flows, an alluvial diagram emphasizes transitions and re-categorizations over sequential stages.

## Best Data Types
- Categorical membership data tracked across multiple discrete time points
- Panel or longitudinal survey data showing group migrations
- Classification changes over sequential stages (e.g., policy status across negotiation rounds)
- Portfolio composition shifts across reporting periods

## When to Use
- Showing how entities shift between categories over time (e.g., countries moving between emission tiers across decades)
- Tracking participant migration between groups in sequential periods
- Visualizing policy or classification changes across discrete milestones
- Comparing categorical compositions at specific snapshots while showing the flows between them

## When NOT to Use
> [!warning] Avoid When
> - You need to show continuous time series — use an [[Area Chart]] or [[Stream Graph]] instead
> - The flow is unidirectional with no re-categorization — a [[Sankey Diagram]] is simpler and clearer
> - You only have two time points — a [[Slope Chart]] is more readable
> - There are too many categories (more than ~8) creating spaghetti-like visual noise
> - The audience needs to read precise values — the flowing bands make exact quantities hard to judge

## Real-World Use Cases
- Voter migration between political parties across election cycles
- Student major changes across academic years
- Customer segment migration in cohort analyses
- Disease classification changes across diagnostic revisions

### Energy & Climate Applications
- **Country Energy Mix Evolution**: How the share of coal, oil, gas, nuclear, hydro, wind, and solar shifts across decades (1990, 2000, 2010, 2020, 2030 projected) for a given country or region
- **Carbon Market Participant Migration**: Tracking how market participants (compliance buyers, voluntary buyers, speculators, offset developers) shift roles across carbon market phases
- **Policy Alignment Shifts Across COP Cycles**: Visualizing how countries move between NDC ambition tiers (insufficient, compatible, aligned, role model) from COP21 through COP30
- **MDB Portfolio Reallocation Over Time**: How multilateral development bank lending shifts across sectors (energy, transport, agriculture, water) across five-year strategy periods
- **Renewable Energy Technology Adoption Stages**: Countries migrating from early adopter to mainstream to saturated categories for solar, wind, and storage across deployment phases

## Visual Style Variations
- **Horizontal time flow**: vertical axes represent time points, bands flow left to right (most common)
- **Color by origin category**: each band retains the color of its starting category, showing where entities came from
- **Color by destination category**: bands take the color of the receiving category, emphasizing where entities end up
- **Highlighted subset**: grey out all flows except a single category's transitions to tell a focused story

## Related Charts
- [[Sankey Diagram]] — similar visual language but designed for system-level flows rather than temporal category migration
- [[Bump Chart]] — shows ranking changes over time with cleaner lines, but loses the proportional width information
- [[Stream Graph]] — shows composition changes as a continuous flow, but without the discrete categorical transition detail

## Inspiration Sources
- [RAWGraphs Alluvial Diagram](https://www.rawgraphs.io/learning/how-to-make-an-alluvial-diagram) — open-source tool with alluvial diagram tutorials
- [Climate Action Tracker Country Assessments](https://climateactiontracker.org/) — NDC rating changes across COP cycles, ideal alluvial source data
- [IRENA Renewable Capacity Statistics](https://www.irena.org/Publications) — country-level capacity data across years for energy mix transitions
- [BloombergNEF Energy Transition Investment](https://about.bnef.com/energy-transition-investment/) — sector investment shifts over time
