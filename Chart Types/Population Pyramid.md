---
title: Population Pyramid
aliases:
  - Age-Sex Pyramid
  - Demographic Pyramid
chart_type: population-pyramid
category: distribution
data_types:
  - categorical
  - continuous
  - paired
data_contexts:
  - Just Transition & Social Impact
  - Renewable Energy & Transition
complexity: medium
audience:
  - policymaker
  - public
  - media
visual_styles:
  - editorial
  - data-journalism
color_approach: diverging
libraries:
  - d3
  - plotly
  - matplotlib
  - datawrapper
effectiveness_rating: null
source_examples: []
has_screenshot: false
has_code_template: false
tags:
  - chart-type/distribution
  - data-type/demographic
  - data-type/categorical
  - data-type/bipolar
  - complexity/intermediate
  - audience/analyst
  - audience/policymaker
  - audience/researcher
  - theme/energy
  - theme/climate
  - theme/supply-chain
  - theme/esg
---

# Population Pyramid

## What It Is
A population pyramid is a mirrored horizontal bar chart that traditionally shows age distribution split by two groups (male/female). Each horizontal bar represents an age cohort, with one group extending left and the other right from a central axis. While originally a demographic tool, the format generalizes powerfully to any two-group comparison across ordered categories — making it valuable for energy workforce analysis, import/export balances, and generation/consumption comparisons.

## Best Data Types
- Two groups compared across an ordered categorical axis (age bands, income brackets, skill levels)
- Demographic distributions (age-sex, age-education)
- Any paired categorical breakdown where left-right contrast is meaningful
- Data with 10-20 ordered categories on the vertical axis

## When to Use
- Comparing the shape of two distributions side by side
- Workforce demographics (age structure of fossil fuel vs. clean energy workers)
- Import vs. export balance by commodity or energy type
- Generation vs. consumption of electricity by fuel type
- When the symmetry or asymmetry between two groups tells the story

## When NOT to Use
> [!warning] Avoid When
> - The categories have no natural order (use [[Tornado Chart]] sorted by value instead)
> - You are comparing more than two groups
> - The vertical axis has fewer than 5 categories (too sparse to form a pyramid shape)
> - The data is not naturally bipolar or paired
> - Precise values matter more than distributional shape

## Real-World Use Cases
- National population structure by age and sex (classic demographic use)
- Customer age distribution: new vs. returning customers
- Education level distribution by gender in a country
- Employee tenure distribution by department

### Energy & Climate Applications
- Energy workforce age distribution: fossil fuel sector (left) vs. clean energy sector (right)
- Import vs. export volumes by energy type (coal, oil, gas, electricity, hydrogen)
- Generation capacity vs. actual generation by fuel type (nameplate vs. realized)
- Male vs. female employment in the energy sector by role category
- Skill level distribution in traditional vs. emerging green jobs

## Visual Style Variations
- **Classic pyramid** — tapered shape with young at bottom, old at top
- **Inverted pyramid** — aging population pattern (wider at top)
- **Symmetric bars** — equal scale on both sides for direct comparison
- **Asymmetric bars** — different scales when one group is much larger

## Related Charts
- [[Tornado Chart]] — same mirrored layout but categories sorted by value, not ordered sequence
- [[Bar Chart]] — one-sided version for single-group distribution
- [[Histogram]] — shows distribution but for continuous data, not paired groups

## Tools That Support This
- **Infogram** — population pyramid template with easy data entry
- **D3.js** — full customization of mirrored bar layout
- **Datylon** — publication-quality population pyramid styling

## Inspiration Sources
- [Infogram Population Pyramid Templates](https://infogram.com/) — ready-made pyramid designs
- [Our World in Data Population Pyramids](https://ourworldindata.org/age-structure) — real demographic examples with context
