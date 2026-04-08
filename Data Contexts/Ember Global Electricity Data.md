---
title: Ember Global Electricity Data
tags:
  - data-context
  - theme/energy-markets
  - theme/renewable-energy
  - theme/climate
  - theme/coal-phase-down
  - reference/ember
---

# Ember Global Electricity Data

## Overview
Ember is an independent energy think tank producing the world's most comprehensive open electricity dataset. Their flagship product — the Electricity Data Explorer — covers 215 countries with generation, demand, capacity, and CO2 emissions data (yearly + monthly for 88 countries). All data is CC BY 4.0 and updated twice monthly. Ember's reports are the global reference for tracking the clean power transition.

## Key Reports
- **Global Electricity Review** (annual) — flagship report covering global generation mix, source trends, major country deep-dives. Key milestone: 40.9% clean power in 2024
- **European Electricity Review** (annual) — EU-focused. Key finding: wind+solar exceeded fossil fuels for first time in 2025 (30% vs 29%)
- **Global Electricity Mid-Year Insights** — half-year update. 2025 finding: renewables overtook coal globally for first time (34.3% vs 33.1%)
- **Indian States Electricity Transition (SET)** — 21 Indian states across 18 parameters, with IEEFA
- **US Electricity Special Report** — wind+solar overtook coal in 24 US states
- **China Energy Transition Review** — 278 GW solar + 80 GW wind added in 2024
- **Reframing Energy for the Age of Electricity** — "electrons vs molecules" framework

## Data Tools Portfolio

| Tool | Scope | Key Feature |
|---|---|---|
| [Electricity Data Explorer](https://ember-energy.org/data/electricity-data-explorer/) | 215 countries | 3 views: Overview, Change between years, Seasonal patterns |
| [2030 Renewable Target Tracker](https://ember-energy.org/data/2030-global-renewable-target-tracker/) | 98 countries | Interactive map of renewable targets by technology |
| [Europe Interconnection Tool](https://ember-energy.org/data/europe-electricity-interconnection-data-tool/) | European grid | Cross-border flows and capacity |
| [Wind & Solar Capacity Explorer](https://ember-energy.org/data/wind-and-solar-capacity-data-explorer/) | 25 countries | Monthly capacity additions (~93% of global solar/wind) |
| [India Electricity Explorer](https://ember-energy.org/data/india-electricity-data-explorer/) | India national + state | Generation, capacity, emissions |
| [India SET Data Tool](https://ember-energy.org/data/india-set-data-tool/) | 21 Indian states | 18 parameters across 3 dimensions |
| [US Electricity Explorer](https://ember-energy.org/data/us-electricity-data-explorer/) | US | US-specific electricity data |

## Data Access
- **CSV downloads** — directly from website
- **REST API** — `api.ember-climate.org/docs` (free API key)
- **R package** — `emberr`
- **License** — CC BY 4.0 (free, open, attribution required)

## Key Metrics
- Electricity generation by source (TWh) — coal, gas, oil, nuclear, hydro, wind, solar, bioenergy, other renewables
- Electricity demand (TWh)
- Installed capacity (GW)
- CO2 emissions from power (Mt CO2)
- Emission intensity (gCO2/kWh)
- Clean power share (%)
- Renewable share (%)
- Per capita generation/demand (kWh/person)

## Ember's Visualization Design System

### Technology Stack
- **Flourish** — primary charting engine for report embeds (interactive)
- **Svelte 5 + LayerCake** — data explorer framework (SVG-based, responsive)
- **d3-scale + d3-shape** — underlying scale and curve functions

### Color Palette (Energy Sources)

| Source | Color | Hex |
|---|---|---|
| Coal (black/bituminous) | Near black | `#121212` |
| Coal (brown/lignite) | Dark brown | `#744A26` |
| Gas (steam) | Orange | `#F48E1B` |
| Gas (CCGT) | Light orange | `#FDB462` |
| Solar (utility) | Bright yellow | `#FED500` |
| Solar (rooftop) | Pale yellow | `#FFF58D` |
| Wind | Forest green | `#2C7629` |
| Hydro | Steel blue | `#5EA0C0` |
| Bioenergy | Teal | `#1D7A7A` |
| Battery (discharge) | Deep blue | `#3245C9` |
| Battery (charge) | Medium blue | `#577CFF` |

> [!tip] Color Logic
> - **Fossil fuels** = warm tones (blacks, browns, oranges) — visually "heavy"
> - **Renewables** = cool/natural tones (green, blue, yellow) — visually "clean"
> - **Solar** gets the most visually prominent color (bright yellow `#FED500`)
> - **Coal** gets the darkest tones — conveying heaviness/pollution

### Brand Identity
- **Primary**: Dark navy (~`#1B2A4A`) for text, navigation, headers
- **Accent**: Bright green (~`#3ECF8E`) for CTAs, active states, logo highlight
- **Background**: Cool grey (~`#F0F2F5`) for page backgrounds
- **Cards**: White (`#FFFFFF`) for chart containers
- **Focus dot**: `#C74523` (Ember's signature orange-red) for hover interactions

### Layout Patterns
- **KPI Highlight Cards** — 3 metrics in a row as hero element (e.g., "22% low-carbon", "10% solar+wind", "78% fossil")
- **Numbered Key Highlights** — 01, 02, 03 callout boxes before analysis text
- **Three-Tab View** — Overview / Change between years / Seasonal patterns
- **Sticky filter bar** — dataset + metric + source + geography filters in one persistent bar
- **Chapter navigation** — collapsible TOC for long-form reports

### Narrative Techniques
- **Milestone framing** — "first time since...", "record...", "overtaking..."
- **Counterfactual comparisons** — "without wind+solar added since 2019, EU would have imported 92bn m3 more gas"
- **S-curve storytelling** — showing exponential growth (solar 100→1000 TWh in 8 years)
- **Threshold tracking** — "59 countries above 20% coal in 2015, down to 40 in 2024"
- **Demand attribution** — decomposing what drove demand growth (heatwaves, EVs, data centres)

## Ember's Chart Types

### Standard Charts Used
- [[Stacked Area Chart]] — generation mix over time (their default view)
- [[Line Chart]] — individual source trends, solar growth curves
- [[Bar Chart]] — year-over-year change, country comparisons
- [[Stacked Bar Chart]] — generation mix breakdown by country
- [[Choropleth Map]] — renewable targets, coal share by country

### Ember-Specific Visualization Patterns
- [[S-Curve Growth Chart]] — exponential technology adoption trajectories
- [[Change Attribution Chart]] — what sources drove year-over-year changes
- [[Threshold Tracker]] — countries crossing a threshold over time
- [[Counterfactual Chart]] — showing "what would have happened without X"
- [[KPI Card Array]] — 3-metric hero element for dashboards
- [[Seasonal Pattern Chart]] — monthly decomposition with year-over-year overlay

## Recommended Chart Types for Ember Data
- [[Stacked Area Chart]] — global generation mix evolution
- [[Line Chart]] — solar/wind growth trajectories, emission intensity decline
- [[Waterfall Chart]] — year-over-year change decomposition by source
- [[Small Multiples]] — same chart for each country/region
- [[Bump Chart]] — country rankings by renewable share over years
- [[Choropleth Map]] — clean power share, emission intensity by country
- [[Sankey Diagram]] — energy flow from source to end-use
- [[Heatmap]] — monthly generation patterns across years
- [[Racing Bar Chart]] — animated country rankings over time

## Related Contexts
- [[Energy Markets]]
- [[Renewable Energy & Transition]]
- [[Climate & Emissions]]
- [[Net Zero Pathways]]
- [[COP UNFCCC IEA]]
