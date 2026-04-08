---
title: Stream Graph
aliases:
  - ThemeRiver
  - Streamgraph
tags:
  - chart-type/temporal
  - data-type/time-series
  - data-type/compositional
  - data-type/categorical
  - complexity/advanced
  - audience/analyst
  - audience/researcher
  - audience/designer
  - theme/energy-markets
  - theme/climate
  - theme/carbon-markets
  - theme/cop-unfccc
  - theme/renewable-energy
category: Temporal
complexity: advanced
best_audience: analysts, researchers, data designers
---

# Stream Graph

## What It Is
A stream graph is a type of stacked area chart that is displaced around a central axis rather than anchored to a baseline. The result is an organic, flowing visualization where each "stream" represents a category, and its thickness at any point encodes its value. The symmetric layout reduces the visual distortion that stacked area charts create for categories placed higher in the stack, making relative size comparisons fairer across all categories.

## Best Data Types
- Multiple time series showing composition or volume evolution
- Categorical data tracked over a continuous time axis where organic visual storytelling is valued
- Data where no single natural baseline exists (e.g., relative growth of topics, genres, or technologies)
- High-category-count temporal data (8-15 categories) where a stacked area chart would be hard to read

## When to Use
- Visualizing the evolution of multiple categories over a long time period with an emphasis on flow and narrative
- Showing how the relative prominence of different topics, technologies, or sources changes over time
- Creating editorial or presentation-quality graphics where visual impact matters
- Exploring data where the aesthetic of organic growth and decline adds meaning (e.g., energy transitions, cultural trends)

## When NOT to Use
> [!warning] Avoid When
> - Precise values or comparisons are required — the floating baseline makes reading exact quantities impossible
> - The audience expects standard business charts — stream graphs have a learning curve
> - You have fewer than 4 categories — an [[Area Chart]] will be clearer and more conventional
> - The data has sharp discontinuities or step changes — the smoothing will misrepresent the data
> - You need to show totals clearly — the symmetric layout obscures the aggregate sum

## Real-World Use Cases
- Music genre popularity over decades (the classic stream graph use case from the New York Times)
- Box office revenue by movie genre across years
- Social media topic volume over time
- Programming language popularity trends

### Energy & Climate Applications
- **Global Energy Source Evolution**: The rise and relative decline of coal, oil, gas, nuclear, hydro, wind, solar, biomass, and geothermal over 50+ years, showing the energy transition as an organic flow
- **Carbon Market Volume by Credit Type**: Volumes of CERs, VERs, EUAs, nature-based credits, tech-based removals, and other credit types across the history of carbon markets
- **Climate Negotiation Topics Across COP Sessions**: Relative prominence of mitigation, adaptation, loss and damage, finance, technology transfer, and transparency topics across COP1 through COP30
- **Renewable Energy Patent Filing Trends**: Patent applications by technology (solar, wind, storage, hydrogen, CCUS, bioenergy) across decades showing innovation waves
- **Energy R&D Spending by Technology**: Government and private R&D expenditure flowing across nuclear, fossil, efficiency, renewables, and hydrogen categories over 40 years

## Visual Style Variations
- **Symmetric (centered) stream**: the classic form, displaced equally above and below a central axis
- **Wiggle-minimized**: algorithmic baseline that minimizes overall stream wiggle for a calmer visual
- **Silhouette (zero-centered)**: symmetric around zero, creating a mirror effect
- **Interactive with tooltip**: digital implementations where hovering reveals precise values for each stream at a given time point

## Related Charts
- [[Area Chart]] — the baseline-anchored version, more conventional and easier to read precise values but less visually dynamic
- [[Alluvial Diagram]] — shows categorical transitions at discrete points rather than continuous flow, better for migration narratives
- [[Ridgeline Plot]] — shows distribution changes over time with overlapping density curves, useful when each category is a distribution rather than a single value

## Inspiration Sources
- [Lee Byron's Original Stream Graph](http://leebyron.com/streamgraph/) — the seminal work that popularized the form
- [IEA Global Energy Review](https://www.iea.org/reports/global-energy-review-2023) — energy source data spanning decades, ideal for stream graph treatment
- [BP Statistical Review of World Energy](https://www.energyinst.org/statistical-review) — now the Energy Institute Statistical Review, with long-run energy source data
- [UNFCCC Topics and Agendas](https://unfccc.int/) — COP negotiation topic data for thematic stream visualization
