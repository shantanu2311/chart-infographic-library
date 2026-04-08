---
title: Choosing the Right Chart
tags:
  - design-principle
  - chart-selection
  - decision-framework
  - data-types
---

# Choosing the Right Chart

## The Principle
Chart selection starts with two questions: what is the data type, and what is the communication purpose? The intersection of these two answers narrows the field to 2-3 viable chart types. The final choice depends on audience familiarity, data density, and the medium (screen, print, presentation).

## Why It Matters
The wrong chart type can hide patterns, mislead readers, or simply confuse. A pie chart with 15 slices is unreadable. A line chart for categorical data implies false continuity. Dual-axis charts suggest correlations that may not exist. Choosing correctly is the highest-leverage design decision -- it determines whether the data communicates or just occupies space.

## Key Guidelines

### By Purpose
- **Compare values** -> [[Bar Chart]], [[Grouped Bar Chart]], [[Dot Plot]], [[Lollipop Chart]]
- **Show change over time** -> [[Line Chart]], [[Area Chart]], [[Slope Chart]], [[Sparkline]]
- **Show composition** -> [[Stacked Bar Chart]], [[Stacked Area Chart]], [[Pie Chart]] (limited), [[Treemap]], [[Marimekko Chart]]
- **Show distribution** -> [[Histogram]], [[Box Plot]], [[Violin Plot]], [[Bee Swarm Plot]]
- **Show relationships** -> [[Scatter Plot]], [[Bubble Chart]], [[Connected Scatter Plot]]
- **Show flow or process** -> [[Sankey Diagram]], [[Alluvial Diagram]], [[Waterfall Chart]]
- **Show geographic patterns** -> [[Choropleth Map]], [[Cartogram]], [[Dot Map]]
- **Show ranking** -> [[Bar Chart]] (sorted), [[Bump Chart]], [[Racing Bar Chart]]
- **Show part-to-whole over time** -> [[Stacked Area Chart]], [[Marimekko Chart]]

### By Data Type
- **One numeric variable** -> histogram, box plot, KPI card
- **Two numeric variables** -> scatter plot, connected scatter, line chart (if one is time)
- **One categorical + one numeric** -> bar chart, dot plot, lollipop chart
- **Time series** -> line chart, area chart, sparkline
- **Hierarchical** -> treemap, sunburst, icicle chart
- **Network/flow** -> Sankey, alluvial, chord diagram

### By Audience
- **General public** -> bar, line, pie (limited), map -- familiar forms only
- **Analysts / domain experts** -> scatter, small multiples, box plots, Sankey -- can handle complexity
- **Executives** -> KPI cards, sparklines, waterfall -- summary-first with drill-down option

## Examples

### Good Practice
> [!tip] Do This
> - Comparing 5 countries' emissions: horizontal bar chart sorted by value, not alphabetically
> - Showing energy mix evolution over 20 years: stacked area chart with consistent color encoding
> - Revealing the relationship between facility size and emission intensity: scatter plot with regression line

### Bad Practice
> [!warning] Avoid This
> - Pie chart with 10+ slices where half are under 3% -- use a bar chart instead
> - 3D charts of any kind for serious analytical work -- they distort perception
> - Dual-axis line charts implying correlation between unrelated metrics (CO2 and stock price)
> - Line chart connecting categorical data (countries) that has no meaningful interpolation between points

## Energy & Climate Applications
- Emission inventory results: waterfall (scope decomposition), stacked bar (source breakdown), KPI cards (headline metrics)
- Technology comparison: grouped bar (cost vs savings), scatter (payback vs CO2 reduction), radar (multi-criteria)
- Policy impact over time: line chart (trend), before/after bar (intervention effect), slope chart (two-point comparison)

## Applicable Chart Types
This principle links to every chart type in the library:
- [[Bar Chart]] | [[Grouped Bar Chart]] | [[Stacked Bar Chart]] | [[Lollipop Chart]]
- [[Line Chart]] | [[Area Chart]] | [[Stacked Area Chart]] | [[Sparkline]] | [[Slope Chart]]
- [[Pie Chart]] | [[Donut Chart]] | [[Treemap]] | [[Marimekko Chart]]
- [[Scatter Plot]] | [[Bubble Chart]] | [[Connected Scatter Plot]]
- [[Histogram]] | [[Box Plot]] | [[Violin Plot]] | [[Bee Swarm Plot]]
- [[Sankey Diagram]] | [[Alluvial Diagram]] | [[Waterfall Chart]]
- [[Choropleth Map]] | [[Cartogram]] | [[Dot Map]]
- [[Heatmap]] | [[Small Multiples]] | [[KPI Card Array]]
- [[Bump Chart]] | [[Racing Bar Chart]] | [[Radar Chart]]

## Tools & Implementation
- **From Data to Viz** (data-to-viz.com) -- interactive decision tree from data type to chart recommendation
- **FT Visual Vocabulary** -- purpose-based chart selection poster used by the Financial Times graphics team
- **Chart Chooser Cards (Stephanie Evergreen)** -- physical/digital cards for workshop-based chart selection

## Further Reading
- [From Data to Viz](https://www.data-to-viz.com/) -- interactive decision tree for chart type selection
- [FT Visual Vocabulary](https://ft.com/vocabulary) -- the Financial Times' chart selection framework
- [The Graphic Continuum (Schwabish & Ribecca)](https://policyviz.com/2014/09/09/graphic-continuum/) -- mapping chart types along a complexity continuum

## Related Principles
- [[Data-Ink Ratio]]
- [[Emphasis and De-emphasis]]
- [[Accessibility in Dataviz]]
- [[Storytelling with Sequence]]
- [[Color for Data]]
- [[Axis Design]]
- [[Chart Titles That Work]]
- [[Legend Placement]]
- [[Typography in Charts]]
- [[Annotation Techniques]]
- [[Small Multiples Patterns]]
- [[Mobile-Responsive Charts]]
- [[Dark Mode Design]]
- [[Brand-Consistent Charts]]
- [[Chart Animation Guidelines]]
