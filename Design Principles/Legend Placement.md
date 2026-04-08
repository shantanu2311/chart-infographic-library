---
title: Legend Placement
tags:
  - design-principle
  - legend
  - labeling
  - layout
---

# Legend Placement

## The Principle
A legend is a lookup table between visual encoding and meaning. The best legend is no legend at all -- direct labeling eliminates the cognitive cost of matching colors to a separate key. When legends are necessary, their placement should minimize eye travel between the data and the key.

## Why It Matters
Every time a reader looks from a chart line to a legend box and back, they lose cognitive momentum. For a chart with 5 series, this lookup happens dozens of times. Direct labeling keeps the reader's attention on the data. When legends are unavoidable, poor placement (below the chart, far from the data) forces excessive eye movement and reduces comprehension speed.

## Key Guidelines
- **Direct label** series whenever space permits -- place the label at the line endpoint or on the largest bar segment
- Use **integrated legends** (inline with the title or subtitle area) to keep color-meaning pairs near the top-left reading entry point
- Place external legends **above or to the right** of the chart, never below (readers may never scroll down to find it)
- Use **horizontal legend layouts** for 2-4 items; switch to vertical for 5+ items
- Make legend items **interactive** in digital contexts: click/tap to filter or highlight the corresponding series
- Match legend **order to data order** -- if series A is on top of the stacked bar, it should be first in the legend
- Color swatches should be **large enough** to identify (minimum 12x12px) and adjacent to the label text
- **Eliminate the legend entirely** for single-series charts -- the title and subtitle carry the meaning

## Examples

### Good Practice
> [!tip] Do This
> - Line chart with 4 series: each line directly labeled at its right endpoint with matching color text -- no legend box
> - Stacked area chart with 3 sources: integrated legend in the subtitle area: "Coal (grey) | Gas (blue) | Solar (amber)"
> - Interactive dashboard: legend items double as filter toggles; clicking "Scope 2" greys out other scopes

### Bad Practice
> [!warning] Avoid This
> - A legend box placed below a long chart, separated by a paragraph of text, requiring scrolling to find it
> - Legend order (alphabetical) contradicting data order (by magnitude), forcing readers to mentally reorder
> - Tiny 8x8px color swatches where similar hues (light blue vs medium blue) are indistinguishable

## Energy & Climate Applications
- Energy mix area charts: direct labels on the rightmost edge of each colored area ("Solar 28%", "Wind 15%", "Coal 42%")
- Scope waterfall: no legend needed -- each step is self-labeled with the scope category name
- Multi-facility comparison: interactive legend lets users click to isolate one facility's data from the group

## Applicable Chart Types
- [[Line Chart]] -- direct endpoint labels eliminate legend; interactive highlight on hover for dense series
- [[Stacked Bar Chart]] -- legend order must match stack order (top-to-bottom or bottom-to-top consistently)
- [[Area Chart]] -- direct labels on the rightmost area edges; integrated legend in subtitle for print
- [[Choropleth Map]] -- continuous color legend (gradient bar) positioned below or beside the map
- [[Scatter Plot]] -- shape + color legend needed when encoding two categorical dimensions
- [[Pie Chart]] -- direct slice labels with leader lines; external legend only if slices are too thin

## Tools & Implementation
- **Recharts `Legend` component** -- configurable position (top, bottom, left, right) with custom icon renderers
- **d3 direct labeling** -- position text elements at series endpoints using `d3.select().text()` with collision detection
- **Figma component variants** -- design legend as a reusable component with horizontal/vertical/integrated variants

## Further Reading
- [Why Directly Labeling Your Line Charts Is Better (Datawrapper)](https://blog.datawrapper.de/direct-labeling-line-charts/) -- evidence for direct labeling over legends
- [FT Visual Vocabulary: Legend Patterns](https://ft.com/vocabulary) -- how the Financial Times handles legend placement

## Related Principles
- [[Color for Data]]
- [[Annotation Techniques]]
- [[Data-Ink Ratio]]
- [[Axis Design]]
