---
title: Minimal & Editorial
tags:
  - visual-style
  - editorial
  - typography
  - policy
  - academic
---

# Minimal & Editorial

## What It Is
A design aesthetic rooted in print journalism and academic publishing, where whitespace is a deliberate compositional element rather than empty space. Every pixel of ink must earn its place. The style trusts the reader's intelligence, letting data speak through restrained typography and muted palettes rather than decorative flourishes.

## Key Characteristics
- Generous whitespace margins (40-80px) creating breathing room between chart elements
- Strong typographic hierarchy using size, weight, and color contrast instead of borders or backgrounds
- Single accent color against a neutral base (slate, charcoal, warm grey)
- Minimal gridlines — often just a baseline axis or light horizontal rules
- Direct labeling on data points instead of legends where possible
- Annotations as first-class citizens, not afterthoughts

## Color Palettes
- **Slate Monochrome**: `#1a1a2e` (headlines), `#4a4a5a` (body), `#8e8e9e` (secondary), `#e74c3c` (single accent) — classic FT approach
- **Warm Newsprint**: `#2c2c2c`, `#5c5c5c`, `#a0a0a0`, `#c8a96e` (gold accent) — evokes broadsheet quality
- **Cool Editorial**: `#0d1b2a`, `#415a77`, `#778da9`, `#e0e1dd` (background), `#ef476f` (highlight) — Bloomberg-influenced
- **Earth Ink**: `#3d3d3d`, `#6b705c`, `#a5a58d`, `#cb997e` (accent) — sustainability reporting warmth

## Typography
- **Headlines**: Serif faces — Charter, Tiempos, GT Sectra, or Freight Display at 28-36px, medium weight
- **Body/Labels**: Clean sans-serif — Inter, Graphik, National, or Soehne at 13-15px, regular weight
- **Data Labels**: Monospace or tabular figures — JetBrains Mono, Fira Code at 11-12px for number alignment
- **Annotation Text**: Italic sans-serif at 12px for contextual notes
- **Line Height**: 1.5-1.6 for body, 1.2-1.3 for headlines

## Best For
- Policy briefs and government white papers
- [[IEA]] World Energy Outlook publications and similar institutional reports
- [[IPCC]] assessment summaries and climate science communication
- Academic papers and peer-reviewed journal figures
- Financial analysis reports (earnings, market outlook)

### Energy & Climate Applications
- Annual GHG inventory reports where clarity of numbers matters most
- Energy transition timeline charts showing policy milestones
- Carbon budget waterfall charts for national and sectoral breakdowns
- Emission factor comparison tables across methodologies ([[IPCC]], [[DEFRA]], [[CEA]])

## Chart Types That Work Well
- [[Line Chart]] — clean trend lines with minimal decoration; perfect for emissions trajectories over decades
- [[Bar Chart]] — simple vertical or horizontal bars with direct value labels; ideal for country/sector comparisons
- [[Slope Chart]] — two-point comparisons that leverage the editorial emphasis on change narratives
- [[Small Multiples]] — grid of mini-charts that let patterns emerge without chart junk
- [[Dot Plot]] — ranked distributions where whitespace between dots carries meaning

## Design Tips
> [!tip] Best Practices
> - Remove every element that does not directly aid comprehension — if you cannot justify a gridline, delete it
> - Use a single accent color for the primary data series and grey for all context/comparison series
> - Place chart titles as full sentences that state the takeaway, not just the topic (e.g., "India's grid emission factor fell 18% since 2015" not "Grid Emission Factors")
> - Align all text and numbers to a baseline grid for visual rhythm
> - Reserve bold weight for exactly one thing: the most important number or label on the chart

## Tools & Software
- [[Datawrapper]] — purpose-built for editorial charts with sensible defaults
- [[ggplot2]] (R) — `theme_minimal()` and `theme_economist()` from ggthemes as starting points
- [[Observable]] / D3.js — full control for bespoke editorial pieces
- [[Figma]] — for static report layouts combining charts with long-form text

## Inspiration Sources
- [Financial Times Visual Journalism](https://www.ft.com/visual-and-data-journalism) — gold standard for editorial data viz
- [The Economist Graphic Detail](https://www.economist.com/graphic-detail) — restrained palette mastery
- [Our World in Data](https://ourworldindata.org/) — clarity-first approach for global datasets
- [IEA Data & Statistics](https://www.iea.org/data-and-statistics) — institutional editorial style

## Related Styles
- [[Data Journalism]]
- [[Corporate & Business]]
- [[Dark Mode & High Contrast]]
