---
title: Bubble Chart
aliases:
  - Bubble Plot
  - Proportional Symbol Chart
tags:
  - chart-type/relationship
  - data-type/continuous
  - data-type/trivariate
  - complexity/intermediate
  - audience/analysts
  - audience/researchers
  - audience/policy-makers
  - theme/emissions
  - theme/energy-transition
  - theme/MDBs
  - theme/climate-finance
category: Relationship
complexity: intermediate
best_audience: analysts, researchers, policy-makers
---

# Bubble Chart

## What It Is
A bubble chart extends the [[Scatter Plot]] by introducing a third variable encoded as the size (area) of each data point. Optionally, a fourth variable can be encoded through bubble color. This creates a rich, multi-dimensional view of data that can reveal complex relationships between three or more variables simultaneously. Popularized by Hans Rosling's Gapminder visualizations, bubble charts are especially powerful for comparing entities across multiple performance dimensions.

## Best Data Types
- Three continuous variables: x-axis, y-axis, and bubble size
- Optionally a fourth variable as bubble color (categorical or continuous)
- Cross-sectional comparisons of entities (countries, companies, projects)
- Data where the relative magnitude of the third variable is important

## When to Use
- Comparing entities across three dimensions simultaneously (e.g., GDP, emissions, population)
- Adding quantitative context to a scatter plot (the third variable provides scale)
- Presentation-quality visualizations where narrative storytelling is important
- When the size dimension adds genuine insight beyond what x and y axes show
- Animated bubble charts for showing multi-dimensional change over time

## When NOT to Use
> [!warning] Avoid When
> - You have too many bubbles (more than 30-40), causing overlap and clutter
> - The third variable (size) does not add meaningful information
> - Precise comparison of bubble sizes is needed (human area perception is imprecise)
> - Two of the three variables are highly correlated, making the size encoding redundant
> - The audience will confuse bubble diameter with bubble area (always scale by area, not radius)

## Real-World Use Cases
- Gapminder: GDP per capita (x) vs life expectancy (y) vs population (size) by country
- Venture capital: funding stage (x) vs valuation (y) vs deal size (size)
- Product comparison: price (x) vs rating (y) vs market share (size)
- City planning: density (x) vs transit access (y) vs population (size)

### Energy & Climate Applications
- Country comparison: GDP per capita (x) vs CO2 emissions per capita (y) vs total population (size), colored by continent
- Technology assessment: levelized cost of energy (x) vs technology readiness level (y) vs global market size (size)
- MDB project portfolio: project IRR (x) vs climate co-benefits score (y) vs project investment size (size)
- Carbon market: carbon price (x) vs market liquidity (y) vs total traded volume (size), colored by market type
- Critical minerals: reserves (x) vs annual production (y) vs projected demand growth (size), colored by country

## Visual Style Variations
- **Standard bubble** — circles on x-y axes with size proportional to the third variable
- **Color-encoded bubble** — bubble color adds a fourth dimension (categorical grouping or continuous gradient)
- **Animated bubble** — Gapminder-style time animation showing movement across dimensions over years
- **Packed bubble** — no axes; bubbles are packed together, sized by one variable, grouped and colored by categories

## Related Charts
- [[Scatter Plot]] — simpler two-variable version; use when the third dimension is not needed
- [[Cartogram]] — geographic alternative where region area is distorted to represent a variable
- [[Dot Plot]] — one-dimensional version for comparing values across categories

## Inspiration Sources
- [Gapminder Tools](https://www.gapminder.org/tools/) — the canonical animated bubble chart for development and emissions data
- [Our World in Data - CO2 and GDP](https://ourworldindata.org/co2-and-greenhouse-gas-emissions) — country-level bubble comparisons
- [BloombergNEF](https://about.bnef.com/) — technology cost and market size bubble visualizations
