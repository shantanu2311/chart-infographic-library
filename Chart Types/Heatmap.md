---
title: Heatmap
aliases:
  - Heat Map
  - Density Matrix
tags:
  - chart-type/relationship
  - data-type/matrix
  - data-type/intensity
  - data-type/temporal
  - complexity/intermediate
  - audience/analysts
  - audience/researchers
  - audience/traders
  - theme/energy-markets
  - theme/carbon-markets
  - theme/emissions
  - theme/renewable-energy
category: Relationship
complexity: intermediate
best_audience: analysts, researchers, traders, operations managers
---

# Heatmap

## What It Is
A heatmap represents data values in a two-dimensional matrix using color intensity. Each cell in the grid corresponds to the intersection of two categorical or ordinal axes, and the cell's color indicates the magnitude of the associated value. Heatmaps excel at revealing patterns, clusters, and anomalies across large matrices of data, making them invaluable for temporal patterns, correlation analysis, and any scenario where a bird's-eye view of a data matrix is needed.

## Best Data Types
- Two-dimensional matrix data (rows x columns) with a continuous intensity value
- Time-based matrices (e.g., hour of day x day of week)
- Correlation matrices (variables x variables)
- Geographic or spatial grids with measured intensities
- Any data that can be organized into a regular grid

## When to Use
- Identifying temporal patterns (peak hours, seasonal trends, day-of-week effects)
- Visualizing correlation or covariance matrices
- Comparing performance across two categorical dimensions simultaneously
- Spotting anomalies, gaps, or clusters in large datasets
- When the sheer volume of data makes individual data points impractical to display

## When NOT to Use
> [!warning] Avoid When
> - The matrix is very small (fewer than 3x3); a simple table would be clearer
> - Precise value reading is critical (color perception is less precise than position or length)
> - The data is not naturally organized into a grid structure
> - Color-blind accessibility is a concern and the color palette has not been carefully chosen
> - You need to show relationships between individual entities (use a [[Network Diagram]] or [[Scatter Plot]])

## Real-World Use Cases
- Website analytics: page views by hour of day and day of week
- Sports: player performance metrics across games
- Genomics: gene expression levels across samples and conditions
- Real estate: price per square foot by neighborhood and property type

### Energy & Climate Applications
- Grid emission factors by region and hour of day, revealing when electricity is cleanest
- Correlation matrix of energy commodity prices: crude oil, natural gas, coal, carbon credits, power
- Seasonal electricity demand patterns: consumption by month (columns) and hour of day (rows)
- Carbon market trading volumes by month and exchange (EU ETS, UK ETS, RGGI, etc.)
- Renewable energy capacity factor by location and month, supporting site selection decisions

## Visual Style Variations
- **Standard heatmap** — rectangular cells with sequential color scale (light to dark)
- **Diverging heatmap** — two-tone color scale centered on zero (e.g., red-white-blue for correlations)
- **Clustered heatmap** — rows and/or columns reordered by hierarchical clustering with dendrograms
- **Calendar heatmap** — GitHub-style contribution grid showing daily values over months

## Related Charts
- [[Correlogram]] — specialized heatmap specifically designed for correlation matrices with additional visual encodings
- [[Scatter Plot]] — use when individual data points and their precise positions matter more than matrix patterns
- [[Choropleth Map]] — geographic heatmap where regions are colored by a data variable

## Inspiration Sources
- [Electricity Maps](https://app.electricitymaps.com/) — real-time grid carbon intensity heatmaps
- [Trading Economics](https://tradingeconomics.com/) — commodity price correlation matrices
- [IEA Electricity Information](https://www.iea.org/data-and-statistics) — hourly and seasonal electricity data
