---
title: Radar Chart
aliases:
  - Spider Chart
  - Web Chart
  - Star Chart
tags:
  - chart-type/comparison
  - data-type/multivariate
  - data-type/numeric
  - complexity/intermediate
  - audience/analyst
  - audience/executive
  - audience/policymaker
  - theme/energy-markets
  - theme/climate
  - theme/net-zero
  - theme/renewable-energy
  - theme/finance
  - theme/cop-unfccc
category: Comparison
complexity: intermediate
best_audience: analyst, executive, policymaker
---

# Radar Chart

## What It Is
A radar chart plots multivariate data on axes radiating from a central point, with each axis representing a different variable. Data points on each axis are connected to form a polygon, and the shape of that polygon reveals the profile of the entity being measured. It is particularly useful for comparing the strengths and weaknesses of entities across multiple dimensions simultaneously, providing an intuitive "fingerprint" of performance.

## Best Data Types
- Multivariate data with 4-10 dimensions per entity
- Normalised or indexed scores (0-100 or 0-1 scale) across dimensions
- Performance profiles, readiness assessments, or maturity models
- Comparative frameworks with standardised rating scales
- Qualitative-to-quantitative scored rubrics

## When to Use
- Comparing the profile shapes of 2-3 entities across multiple dimensions
- Displaying balanced scorecard or maturity assessment results
- Showing where an entity excels or falls short relative to peers
- Presenting multidimensional readiness or risk frameworks
- When the holistic shape of the profile is as important as individual values

## When NOT to Use
> [!warning] Avoid When
> - You have more than 3 overlapping entities (the chart becomes an unreadable tangle)
> - Axes have different scales or units that have not been normalised
> - You have fewer than 4 or more than 12 axes (too few looks odd, too many becomes dense)
> - Precise value reading is critical (radar charts sacrifice precision for pattern recognition)
> - The audience is unfamiliar with the format and will struggle to interpret area and shape
> - Variables have no logical grouping or the ordering of axes is arbitrary (axis placement affects perceived shape)

## Real-World Use Cases
- Product feature comparison across competing offerings
- Employee competency profiles in 360-degree reviews
- City liveability index dimensions (safety, transport, healthcare, education, environment)
- Nutritional profile comparison of food products

### Energy & Climate Applications
- Country energy transition readiness scores across dimensions (policy, investment, technology, infrastructure, social) from WEF Energy Transition Index
- Technology maturity profiles for emerging clean energy solutions (TRL, cost competitiveness, scalability, supply chain readiness, policy support)
- ESG rating dimension comparison for energy companies (environmental, social, governance sub-scores from MSCI, Sustainalytics)
- UNFCCC national adaptation readiness across pillars (institutional, financial, technological, informational, social)
- IEA clean energy investment climate assessment across indicators (regulatory stability, grid access, financing availability, workforce skills, permitting speed)

## Visual Style Variations
- **Filled radar** — the polygon area is shaded with transparency, making it easy to see overlap between entities
- **Outlined radar** — only the polygon border is drawn, reducing visual clutter when comparing multiple entities
- **Radar with benchmarks** — a reference polygon (e.g., sector average or best-in-class) is drawn as a dashed line for comparison
- **Small multiples radar** — individual radar charts per entity arranged in a grid for comparison without overlap

## Related Charts
- [[Bar Chart]] — an alternative for multivariate comparison that sacrifices the holistic shape for precision
- [[Parallel Coordinates]] — another multivariate comparison that uses parallel vertical axes; handles more variables and entities
- [[Dot Plot]] — for comparing entities on individual dimensions with greater precision

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [World Economic Forum — Energy Transition Index](https://www.weforum.org/publications/fostering-effective-energy-transition-2024/) — country radar profiles
- [MSCI ESG Ratings](https://www.msci.com/our-solutions/esg-investing/esg-ratings) — multidimensional ESG scoring
