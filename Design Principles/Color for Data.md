---
title: Color for Data
tags:
  - design-principle
  - color
  - palette
  - accessibility
---

# Color for Data

## The Principle
Color is the most powerful visual channel in data visualization, but also the most misused. Effective color use encodes data accurately, guides attention, and remains accessible to all viewers including the 8% of men and 0.5% of women with color vision deficiency.

## Why It Matters
Poor color choices can mislead readers, hide patterns, or exclude audiences. Sequential palettes must feel linear in perceived lightness. Diverging palettes need a clear neutral midpoint. Categorical palettes must be distinguishable at a glance. Getting color right is the difference between a chart that communicates and one that confuses.

## Key Guidelines
- Use **sequential** palettes (light to dark) for ordered data like temperature or emission intensity
- Use **diverging** palettes (two hues with neutral midpoint) for data with a meaningful center like anomalies or year-over-year change
- Use **categorical** palettes (distinct hues) for nominal data; limit to 6-8 colors before grouping into "Other"
- Ensure **perceptual uniformity** so equal data differences produce equal perceived color differences (use CIELAB/HCL, not RGB)
- Always test with a colorblind simulator (Coblis, Viz Palette) before publishing
- Use **monochrome** when comparing magnitudes within one category; multi-color only when encoding distinct categories
- Reserve red for negative/danger and green for positive/growth only when cultural context supports it
- Add a secondary channel (pattern, label, shape) so color is never the sole differentiator

## Examples

### Good Practice
> [!tip] Do This
> - Ember's energy source palette: coal (dark grey), gas (lighter grey), solar (amber), wind (teal), hydro (blue) -- each source instantly recognizable, colorblind safe
> - Using a single-hue sequential ramp (e.g., light blue to navy) for emission intensity on a choropleth
> - Greying out all series except the one being discussed to direct focus

### Bad Practice
> [!warning] Avoid This
> - Using a rainbow palette for temperature data, which has perceptual banding artifacts and is inaccessible
> - Encoding 12 categories with 12 similar-saturation hues that blur together in small chart areas
> - Red-green encoding without any secondary differentiator (pattern, shape, or direct label)

## Energy & Climate Applications
- Grid emission factor maps: sequential palette from green (low carbon) to brown (high carbon) with perceptually uniform steps
- Energy mix area charts: categorical palette where fossil fuels cluster in warm greys and renewables in distinct cool/warm hues
- Year-over-year emission change: diverging palette centered on zero, with blue for reduction and orange for increase

## Applicable Chart Types
- [[Choropleth Map]] -- sequential or diverging palette encodes geographic variation
- [[Stacked Area Chart]] -- categorical palette distinguishes fuel/energy sources over time
- [[Heatmap]] -- sequential palette maps intensity across two dimensions
- [[Pie Chart]] -- categorical palette must be distinguishable in adjacent slices
- [[Line Chart]] -- color differentiates series; limit to 4-5 before using direct labels
- [[Scatter Plot]] -- color encodes a third variable (category or continuous)

## Tools & Implementation
- **Viz Palette** (Susie Lu) -- test categorical palettes for colorblind safety and name-ability
- **ColorBrewer 2.0** -- curated sequential, diverging, and categorical palettes with accessibility ratings
- **chroma.js** -- JavaScript library for perceptually uniform color interpolation in code

## Further Reading
- [Viz Palette](https://projects.susielu.com/viz-palette) -- interactive palette tester with colorblind simulation
- [ColorBrewer](https://colorbrewer2.org/) -- classic palette tool by Cynthia Brewer
- [Your Friendly Guide to Colors in Data Visualisation](https://blog.datawrapper.de/colorguide/) -- Lisa Charlotte Muth's comprehensive guide

## Related Principles
- [[Accessibility in Dataviz]]
- [[Dark Mode Design]]
- [[Brand-Consistent Charts]]
- [[Emphasis and De-emphasis]]
