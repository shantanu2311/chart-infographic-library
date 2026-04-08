---
title: Ember
tags:
  - source-organization
  - energy
  - electricity
  - open-data
  - climate
---

# Ember

## Overview
Ember is an independent energy think tank focused on accelerating the global electricity transition from coal to clean energy. They produce some of the most widely cited electricity data globally, tracking power generation across 200+ countries. Their data underpins analysis by the IEA, World Bank, and major media outlets.

## Signature Visual Style
- **Color palette**: Navy (#1B2A4A) and green (#3ECF8E) brand identity. Fuel-specific encoding: coal=#121212, solar=#FED500, wind=#2C7629, hydro=#5EA0C0, gas=#E67E22, nuclear=#9B59B6
- **Typography**: Clean sans-serif, moderate weight headings, tabular figures for data labels
- **Layout**: Three-tab data explorers (chart / table / map), full-width responsive containers, KPI card rows above main chart
- **Tone**: Analytical but accessible, advocacy-adjacent without being preachy

## Strengths
- Unmatched global electricity generation dataset updated monthly
- Consistent fuel-color encoding across all publications creates instant recognition
- Open data philosophy with CC BY 4.0 licensing on all datasets
- Strong narrative framing around transition milestones and tipping points
- Effective use of [[Small Multiples]] for cross-country electricity mix comparisons

## Chart Types They Favor
- [[Stacked Area Chart]] — electricity generation mix over time, showing coal displacement by renewables
- [[Line Chart]] — trend tracking for individual fuel shares, demand growth, emissions intensity
- [[Change Attribution Chart]] — decomposing year-on-year changes into contributing factors (demand, fuel switching, efficiency)
- [[KPI Card Array]] — headline metrics (e.g., "Wind+Solar share: 30%") displayed as prominent card rows
- [[Small Multiples]] — country-level electricity breakdowns in grid layout for regional comparisons
- [[Choropleth Map]] — geographic distribution of coal phase-out progress or renewable share
- [[Seasonal Pattern Chart]] — monthly generation patterns revealing seasonal wind/solar complementarity

## Design Patterns Worth Studying
- **Three-tab explorer**: Every major dataset gets chart, table, and map views with synchronized filtering
- **Threshold tracking**: Horizontal reference lines marking key milestones (e.g., "50% clean power")
- **Counterfactual framing**: Showing what emissions would have been without renewables growth
- **S-curve narrative**: Framing technology adoption as S-curves with "tipping point" annotations
- **Milestone markers**: Timeline annotations highlighting when countries crossed key thresholds

## Energy & Climate Relevance
Core to the energy transition narrative. Ember's Global Electricity Review is the definitive annual snapshot of where the world's power sector stands. Their coal-to-clean tracking directly supports Scope 2 analysis, grid emission factor research, and renewable energy target monitoring.

## Key Reports / Products
- **Global Electricity Review** — Annual flagship report covering 200+ countries, electricity generation by source, CO2 emissions
- **European Electricity Review** — EU-focused deep dive with monthly updates
- **India State Electricity Transition (SET)** — State-level electricity data for India
- **Data Explorer** — Interactive tool for exploring electricity generation, capacity, and emissions data
- **Yearly Electricity Data** — Downloadable country-level datasets with monthly granularity

## Data Access
- All data available under CC BY 4.0 license
- Bulk CSV downloads from data catalogue
- API access for programmatic queries
- R package (`ember`) for direct analysis
- GitHub repositories with methodology documentation

## Related Sources
- [[IEA]]
- [[Our World in Data]]
- [[Climate Action Tracker]]
- [[Global Carbon Project]]
