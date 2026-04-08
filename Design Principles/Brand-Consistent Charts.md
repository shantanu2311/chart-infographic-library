---
title: Brand-Consistent Charts
tags:
  - design-principle
  - brand
  - identity
  - templates
---

# Brand-Consistent Charts

## The Principle
Brand-consistent charts apply an organization's visual identity -- colors, typography, logo placement, and design language -- to data visualization without compromising data clarity. The brand should be present but never compete with the data for attention.

## Why It Matters
Charts in reports, dashboards, and presentations represent the organization. Inconsistent styling (random colors, mixed fonts, no logo) looks unprofessional and undermines trust in the data. A branded chart template system ensures every output is instantly recognizable while maintaining the design discipline needed for clear data communication.

## Key Guidelines
- Define a **branded data palette** derived from brand colors but optimized for data use (sufficient contrast, colorblind safe)
- Use the **brand typeface** for titles and navigation; use a neutral sans-serif (Inter, system font) for data labels if the brand font has poor tabular figures
- Place logos in a **consistent position** (top-right or bottom-left) at small size; never let the logo compete with the chart
- Build a **chart template library** (Figma components, Recharts theme config, ggplot theme) that enforces brand tokens
- Maintain **one primary accent color** for emphasis and call-to-action elements; use neutral palette for data
- Balance brand expression with **data clarity** -- if brand colors create accessibility problems, adapt them for data use
- Create **branded export templates** for PDF, PowerPoint, and social media with pre-set dimensions and logo placement
- Document the system in a **data visualization style guide** alongside the brand book

## Examples

### Good Practice
> [!tip] Do This
> - Ember's system: dark navy (#0D1B2A) backgrounds, signature green (#4ECDC4) for renewables, warm amber for solar, consistent Inter font across all reports and dashboards
> - MDB reports: corporate blue primary, grey secondary, logo bottom-right at 40px height, source attribution in consistent position below every chart
> - A Recharts theme config file that sets default colors, fonts, and spacing so every developer-generated chart is on-brand

### Bad Practice
> [!warning] Avoid This
> - Every chart in a report using different colors because each analyst chose their own palette
> - A giant logo watermarked across the center of a chart, obscuring the data
> - Using the brand's decorative display font for axis tick labels, creating legibility problems at small sizes

## Energy & Climate Applications
- Corporate sustainability reports (BRSR, CDP, GRI): branded chart templates ensure visual consistency across 50+ charts in a single report
- Client-facing emission audit deliverables: branded PDF exports with logo, disclaimer, and consistent color encoding for scopes
- Conference presentations: branded slide templates with chart placeholder areas sized for optimal projection

## Applicable Chart Types
- [[Bar Chart]] -- brand primary color for main series, brand grey for comparison/benchmark
- [[Line Chart]] -- brand accent color for the focal series, lighter brand shades for context series
- [[KPI Card Array]] -- brand typography for large metrics, brand accent for trend indicators
- [[Waterfall Chart]] -- brand green for reductions, brand red/orange for increases, brand grey for total
- [[Pie Chart]] -- brand palette for slices, ordered by brand color hierarchy
- [[Area Chart]] -- brand palette with appropriate opacity levels for overlapping areas

## Tools & Implementation
- **Figma design tokens** -- define brand chart tokens (colors, fonts, spacing) as a shared library across design and engineering
- **Recharts theme wrapper** -- create a `<BrandedChart>` component that injects default props for colors, fonts, and margins
- **Style guide generator** -- tools like Storybook or Supernova to document and distribute the chart brand system

## Further Reading
- [Data Visualization Style Guidelines (Urban Institute)](https://urbaninstitute.github.io/graphics-styleguide/) -- exemplary public data viz style guide
- [Ember's Global Electricity Review](https://ember-climate.org/insights/research/global-electricity-review-2024/) -- consistent brand application across dozens of charts

## Related Principles
- [[Color for Data]]
- [[Typography in Charts]]
- [[Dark Mode Design]]
- [[Chart Titles That Work]]
