---
title: Typography in Charts
tags:
  - design-principle
  - typography
  - legibility
  - formatting
---

# Typography in Charts

## The Principle
Typography in charts serves a functional role: it labels, annotates, and titles. Every text element must earn its place through clear hierarchy, appropriate sizing, and number formatting that reduces cognitive load. The font should be invisible -- readers should absorb the data, not notice the typeface.

## Why It Matters
Bad typography is the fastest way to make a professional chart look amateur. Cramped axis labels, inconsistent number formatting, or decorative fonts destroy legibility. A clear typographic hierarchy (title > subtitle > axis label > tick label > annotation) lets readers parse the chart in the correct order, from overview to detail.

## Key Guidelines
- Use **sans-serif** typefaces for digital (Inter, DM Sans, IBM Plex Sans); serif only for print editorial contexts
- Establish a **weight hierarchy**: bold 18-24px for title, regular 14-16px for subtitle, medium 12-14px for axis labels, regular 10-12px for tick marks
- **Minimum readable size**: 10px on desktop, 12px on mobile -- never go below
- Format numbers with **thousands separators** (1,234 not 1234) and consistent decimal places
- Use **abbreviations** for large numbers: 1.2M, 3.4B, 450K -- with the unit defined once in the axis label
- Right-align numeric columns; left-align text labels
- Limit chart text to **two typefaces maximum** (one for data, one for narrative)
- Avoid vertical or angled text; if axis labels don't fit horizontally, rotate the chart or abbreviate

## Examples

### Good Practice
> [!tip] Do This
> - Title in semibold 20px: "India's Grid Emission Factor by Region, FY2024"
> - Subtitle in regular 14px grey: "tCO2e per MWh | Source: CEA v21.0"
> - Axis ticks in regular 11px: "200K", "400K", "600K" with unit "tCO2e" in axis title only once
>
> KPI cards using tabular/monospaced figures so digits align vertically: 1,234.56 stacks cleanly above 12,345.67

### Bad Practice
> [!warning] Avoid This
> - Using Comic Sans or decorative script fonts in any data visualization context
> - Axis labels at 8px that become illegible on projection screens or mobile devices
> - Inconsistent formatting: "1,200 tonnes" on one axis and "1200 T" on another in the same dashboard
> - Rotated text at 45 degrees creating a saw-tooth pattern that slows reading

## Energy & Climate Applications
- Emission values: always show units (tCO2e, MtCO2e, GtCO2e) with appropriate scale abbreviation
- Financial year labels on time axes: "FY22-23" format for Indian reporting contexts
- Grid region labels: standardized abbreviations (NR, WR, SR, ER, NER) with a legend on first use

## Applicable Chart Types
- [[KPI Card Array]] -- large display numbers with unit labels demand precise typographic hierarchy
- [[Small Multiples]] -- panel titles must be compact yet readable across a grid
- [[Bar Chart]] -- axis tick labels and direct bar labels compete for space; hierarchy resolves conflicts
- [[Line Chart]] -- series labels (direct or legend) need to be distinguishable at small sizes
- [[Waterfall Chart]] -- step labels along the x-axis require careful sizing and abbreviation

## Tools & Implementation
- **Google Fonts: Inter** -- free, variable-weight sans-serif with tabular figures; ideal for chart text
- **Figma / Tokens Studio** -- define a type scale token set (chart-title, chart-subtitle, chart-axis, chart-tick) for consistency
- **d3-format / Intl.NumberFormat** -- programmatic number formatting with locale-aware separators

## Further Reading
- [Practical Typography by Matthew Butterick](https://practicaltypography.com/) -- foundational typographic principles
- [Typography for Data Visualisation](https://www.darkhorseanalytics.com/blog/data-looks-better-naked) -- Dark Horse Analytics' design approach

## Related Principles
- [[Annotation Techniques]]
- [[Chart Titles That Work]]
- [[Mobile-Responsive Charts]]
- [[Axis Design]]
