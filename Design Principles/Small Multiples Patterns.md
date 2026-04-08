---
title: Small Multiples Patterns
tags:
  - design-principle
  - small-multiples
  - faceting
  - comparison
---

# Small Multiples Patterns

## The Principle
Small multiples display the same chart type repeated across panels, each showing a different slice of the data (by category, time period, or geography). The consistent structure lets the reader's eye compare patterns across panels without re-learning the visual encoding for each one.

## Why It Matters
When you have more than 4-5 categories on a single chart, overlap and clutter destroy readability. Small multiples solve this by giving each category its own panel while maintaining shared scales so comparisons remain valid. The reader makes comparisons through position and shape rather than wrestling with tangled spaghetti lines or overloaded legends.

## Key Guidelines
- **Share axes** across all panels by default -- consistent x and y scales make comparison possible
- Use **independent y-axes** only when magnitudes differ wildly AND the goal is to compare shapes, not levels
- Arrange panels in a **logical order**: alphabetical, by magnitude, chronological, or geographic
- Keep **panel count** manageable: 4-16 panels works well; beyond 20, consider aggregation or filtering
- Use a **grid layout**: rows x columns where the longer dimension matches reading direction (left-to-right, then top-to-bottom)
- Label each panel with a **concise title** (category name) positioned consistently (top-left of each panel)
- Minimize **per-panel chrome**: one shared axis label set at the bottom/left edges, not repeated in every panel
- **Highlight one panel** against greyed-out others when telling a story about a specific category

## Examples

### Good Practice
> [!tip] Do This
> - 10 panels showing emission trends (2015-2024) for 10 steel-producing states, same y-axis (0-50 MtCO2e), shared x-axis, one grey reference line for national average
> - 6 panels of energy mix area charts (one per grid region: NR, WR, SR, ER, NER, National) with identical color encoding
> - Highlighting Gujarat's panel in full color while greying out the other 9 states to tell a focused story

### Bad Practice
> [!warning] Avoid This
> - Using different y-axis scales per panel without clearly marking it, leading readers to false magnitude comparisons
> - Cramming 30 panels into a single view where each panel becomes too small to read any values
> - Repeating full axis labels, tick marks, and gridlines in every panel, wasting space and adding visual noise

## Energy & Climate Applications
- Country-level emission trajectories: one panel per country, shared 1990-2030 x-axis, highlighting which countries peaked and when
- Facility-level Scope 1 breakdown: one panel per facility showing fuel-type composition, revealing which facilities are outliers
- Monthly electricity generation by source: 12 panels (one per month) showing seasonal variation in solar, wind, and thermal contribution

## Applicable Chart Types
- [[Small Multiples]] -- the core pattern itself
- [[Line Chart]] -- most common use case; trend comparison across categories
- [[Bar Chart]] -- faceted bars for comparing distributions across groups
- [[Area Chart]] -- composition comparison across categories with shared time axis
- [[Scatter Plot]] -- relationship patterns across subgroups

## Tools & Implementation
- **ggplot2 `facet_wrap()` / `facet_grid()`** -- the gold standard for declarative small multiples in R
- **Observable Plot `facet`** -- JavaScript equivalent with automatic axis sharing
- **Recharts** -- manually render an array of chart components in a CSS Grid layout with shared domain props

## Further Reading
- [Small Multiples (Edward Tufte)](https://www.edwardtufte.com/tufte/books_vdqi) -- original formulation in The Visual Display of Quantitative Information
- [How to Use Small Multiples (Storytelling with Data)](https://www.storytellingwithdata.com/blog/2020/3/2/small-multiples) -- practical guidance with examples

## Related Principles
- [[Mobile-Responsive Charts]]
- [[Axis Design]]
- [[Emphasis and De-emphasis]]
- [[Color for Data]]
