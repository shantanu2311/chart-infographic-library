---
title: Annotation Techniques
tags:
  - design-principle
  - annotation
  - context
  - storytelling
---

# Annotation Techniques

## The Principle
Annotations embed context directly into the chart so readers don't have to look elsewhere for explanations. They transform a chart from a raw data display into a guided narrative by marking events, explaining anomalies, and directing the reader's eye to what matters most.

## Why It Matters
A chart without annotations forces readers to guess why a line spiked or a bar dropped. Annotations bridge the gap between data and understanding. The best data journalism -- FT, NYT, Economist -- uses annotations extensively because they reduce the time from "what happened?" to "why it happened" to near zero.

## Key Guidelines
- **Direct label** data series on the chart itself rather than using a separate legend when feasible (fewer than 5 series)
- Use **callout boxes** with leader lines for important data points that need narrative explanation
- Add **reference lines** for benchmarks, targets, or thresholds (e.g., Paris Agreement 1.5C target)
- Place **event markers** (vertical lines with labels) on time series to mark policy changes, crises, or milestones
- Write annotations in **plain language**, not technical jargon -- they are for the reader, not the analyst
- Keep annotations **short**: 5-15 words per callout; use a footnote for longer explanations
- Position annotations to **avoid occluding data** -- use connector lines to place text in whitespace
- Use a **lighter font weight or smaller size** than the title so annotations don't compete with the main message

## Examples

### Good Practice
> [!tip] Do This
> - A vertical dashed line on an emission trend chart labeled "COVID-19 lockdown" at March 2020 with a small note: "Industrial output fell 38%"
> - Direct labeling the final point of each line in a multi-series chart with the country name, eliminating the legend entirely
> - A horizontal reference line at the sector benchmark with the label "BEE PAT target: 1.8 tCO2e/t steel"

### Bad Practice
> [!warning] Avoid This
> - Adding 15 annotations to a single chart, creating visual clutter worse than no annotations at all
> - Using annotations that simply restate what the data already shows: "This bar is taller" -- add the WHY instead
> - Placing annotation text directly on top of data points, making both unreadable

## Energy & Climate Applications
- Marking COP events (COP21 Paris, COP26 Glasgow, COP28 Dubai) on global emission trend lines to show policy impact
- Annotating price spikes on energy commodity charts: "Russia-Ukraine conflict: gas prices +300%"
- Adding BEE PAT benchmark reference lines on facility-level emission intensity charts

## Applicable Chart Types
- [[Line Chart]] -- event markers on time axis, direct series labels at endpoints
- [[Area Chart]] -- callout boxes explaining composition changes at key moments
- [[Scatter Plot]] -- labeling notable outliers with context (e.g., "Plant X: pre-retrofit baseline")
- [[Waterfall Chart]] -- annotating the largest contributing steps with percentage impact
- [[Bar Chart]] -- reference lines for targets or benchmarks across categories

## Tools & Implementation
- **Rough Notation** (JS library) -- hand-drawn-style highlights and annotations for web charts
- **Figma annotation plugins** -- for static chart production with precise callout placement
- **Recharts `ReferenceLine` + `Label`** -- programmatic reference lines and annotations in React

## Further Reading
- [Storytelling with Data: Annotation](https://www.storytellingwithdata.com/blog/2018/1/22/88-annotated-line-graphs) -- Cole Nussbaumer Knaflic's annotation examples
- [The FT Visual Vocabulary](https://ft.com/vocabulary) -- annotation patterns used by the Financial Times

## Related Principles
- [[Typography in Charts]]
- [[Storytelling with Sequence]]
- [[Chart Titles That Work]]
- [[Emphasis and De-emphasis]]
