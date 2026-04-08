---
title: Our World in Data
tags:
  - source-organization
  - open-data
  - academic
  - global-development
  - climate
---

# Our World in Data

## Overview
Our World in Data (OWID) is a research organization based at the University of Oxford, presenting empirical research on the world's largest problems. Founded by Max Roser, it covers everything from poverty and health to energy and CO2 emissions. Their interactive data explorers have become the default reference for evidence-based global analysis, combining academic rigor with radical openness.

## Signature Visual Style
- **Color palette**: Light grey (#f2f2f2) backgrounds, muted but distinct country/category colors from a carefully curated palette. Emphasis through saturation rather than hue changes
- **Typography**: Serif titles (Playfair Display), sans-serif body (Lato). Clear typographic hierarchy separating narrative text from chart annotations
- **Layout**: Long-form article pages with embedded interactive charts. Minimal chrome, generous margins, charts expand to full width. Toggle controls inline with narrative
- **Tone**: Academic, evidence-driven, patient and explanatory. Optimistic without minimizing problems

## Strengths
- Every dataset fully open (CC BY) with GitHub repositories for reproducibility
- Interactive data explorers allowing per-capita, absolute, and logarithmic toggles on any chart
- Extraordinary historical depth — many series go back centuries with careful source stitching
- Consistent methodology documentation alongside every visualization
- Pioneered the "interactive article" format that others now emulate

## Chart Types They Favor
- [[Line Chart]] — multi-country time series with hover-to-highlight, their most common chart type
- [[Stacked Area Chart]] — global composition over time (energy mix, emissions by region, causes of death)
- [[Scatter Plot]] — bivariate relationships (GDP vs emissions, income vs life expectancy) with bubble size and play-over-time
- [[Choropleth Map]] — world maps for any indicator with year slider, the entry point to most topics
- [[Bar Chart]] — country rankings, categorical comparisons, often horizontal with direct labeling

## Design Patterns Worth Studying
- **Interactive data explorers**: Charts with country selectors, per-capita toggles, log-scale switches, and year sliders all in one component
- **Per-capita toggle**: Nearly every chart offers absolute vs per-capita view, fundamentally changing the story
- **Long-run historical framing**: Starting time series from 1800 or earlier to show the full arc of change
- **Extensive annotations**: Direct labels, reference lines, and contextual notes embedded in chart area rather than legends
- **Source transparency**: Every chart links to the underlying data, code, and methodology page

## Energy & Climate Relevance
OWID's CO2 and energy pages are among the most visited resources on climate data globally. Their emissions data (built on Global Carbon Project figures) supports per-capita comparisons, historical responsibility analysis, and sector-level breakdowns. Essential for contextualizing any GHG inventory within global and national trends.

## Key Reports / Products
- **CO2 and Greenhouse Gas Emissions** — Comprehensive topic page with dozens of interactive charts on global emissions
- **Energy** — Production, consumption, and electricity data by country with interactive explorers
- **Climate Change** — Temperature records, sea level, extreme weather, and climate impacts
- **Data Explorer platform** — Grapher tool powering all interactive visualizations, open-source on GitHub
- **ETL pipeline** — Open-source data pipeline stitching hundreds of sources into harmonized datasets

## Data Access
- All data CC BY licensed, free to use with attribution
- GitHub repositories for every dataset with full processing code
- Grapher tool is open source (github.com/owid)
- Bulk CSV downloads from GitHub data catalog
- No formal API, but GitHub raw file URLs serve as pseudo-API endpoints

## Related Sources
- [[Ember]]
- [[Global Carbon Project]]
- [[The Economist]]
- [[Datawrapper]]
