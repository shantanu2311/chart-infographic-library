---
title: Mobile-Responsive Charts
tags:
  - design-principle
  - responsive
  - mobile
  - layout
---

# Mobile-Responsive Charts

## The Principle
Charts must adapt gracefully to screen sizes from 375px mobile to 2560px desktop. Responsive chart design is not just shrinking -- it requires rethinking density, interaction, labeling, and layout to ensure the data remains readable and usable at every breakpoint.

## Why It Matters
Over 60% of web traffic is mobile. A chart designed for desktop that simply scales down becomes unreadable: labels overlap, touch targets are too small, and dense data becomes a blur. Separate mobile and desktop considerations ensure your data reaches all audiences effectively.

## Key Guidelines
- Design **mobile-first**, then add complexity for larger screens
- Switch from **side-by-side** to **stacked** layouts below 768px (bars, small multiples, KPI cards)
- Increase **minimum font size** to 12px on mobile (vs 10px desktop)
- Ensure **touch targets** are at least 44x44px for interactive elements (tooltips, filters, legend items)
- Reduce **data density**: show fewer tick marks, abbreviate labels, aggregate data points on mobile
- Use **vertical scrolling** instead of horizontal scrolling -- mobile users expect vertical flow
- Replace complex charts with **sparklines** or **KPI summary cards** on the smallest screens
- Test at standard social media sizes: **1080x1080** (Instagram), **1200x675** (Twitter/X), **1080x1920** (Stories)

## Examples

### Good Practice
> [!tip] Do This
> - A grouped bar chart on desktop becomes a horizontal stacked bar on mobile, with the category labels fully readable
> - Small multiples in a 4-column grid on desktop reflow to a 1-column vertical list on mobile, each panel taking full width
> - Interactive tooltips on desktop become always-visible direct labels on mobile where hover doesn't exist

### Bad Practice
> [!warning] Avoid This
> - A 12-column data table that requires horizontal scrolling on mobile with no responsive alternative
> - Tiny legend swatches (10x10px) that are impossible to tap on touch devices
> - Relying on hover-only interactions (tooltips, highlight) with no tap/touch fallback

## Energy & Climate Applications
- Emission dashboard: desktop shows full waterfall + scope breakdown side by side; mobile stacks them vertically with a summary KPI card on top
- Energy mix area chart: desktop shows 25-year timeline; mobile shows latest 5 years with a "view full history" expand option
- Funding directory: desktop shows a filterable card grid; mobile shows a searchable vertical list with expandable detail sections

## Applicable Chart Types
- [[Bar Chart]] -- horizontal bars work better on mobile; vertical bars need fewer categories
- [[Line Chart]] -- reduce to key series on mobile; add "show all" toggle
- [[Small Multiples]] -- reflow from grid to single-column stack
- [[KPI Card Array]] -- 4-across on desktop to 2-across or stacked on mobile
- [[Pie Chart]] -- consider replacing with horizontal bar on very small screens
- [[Choropleth Map]] -- ensure pan/zoom controls are touch-friendly; add a ranked list alternative

## Tools & Implementation
- **CSS Container Queries** -- responsive chart wrappers that adapt based on container width, not viewport
- **Recharts `ResponsiveContainer`** -- wraps charts to fill parent width; combine with breakpoint-aware prop changes
- **Figma Auto Layout** -- prototype responsive chart layouts before development

## Further Reading
- [Responsive Data Visualization (Bocoup)](https://bocoup.com/blog/responsive-data-visualization) -- engineering approaches to responsive charts
- [Designing Charts for Mobile (Lisa Charlotte Muth)](https://blog.datawrapper.de/weekly-chart-mobile/) -- practical mobile chart design advice

## Related Principles
- [[Small Multiples Patterns]]
- [[Typography in Charts]]
- [[Axis Design]]
- [[Legend Placement]]
