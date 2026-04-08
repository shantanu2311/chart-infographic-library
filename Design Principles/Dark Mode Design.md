---
title: Dark Mode Design
tags:
  - design-principle
  - dark-mode
  - theming
  - contrast
---

# Dark Mode Design

## The Principle
Dark mode inverts the traditional light canvas: data and text appear as lighter elements on a dark background. This is not simply inverting colors -- it requires rethinking contrast, saturation, and element hierarchy to maintain readability and avoid visual fatigue on dark surfaces.

## Why It Matters
Dark mode is standard in modern dashboards, developer tools, presentation decks, and mobile apps. Over 80% of smartphone users enable dark mode. A chart designed for white backgrounds will look washed out, low-contrast, or garish on dark surfaces. Dedicated dark mode design ensures your charts work in both contexts, which is especially important for dashboards viewed in dimly lit environments.

## Key Guidelines
- Avoid **pure white (#FFFFFF) on pure black (#000000)** -- the extreme contrast causes halation (glowing text); use off-white (#E8E8E8) on dark grey (#1A1A2E or #1E1E2E)
- **Reduce saturation** of bright colors by 10-20% on dark backgrounds to prevent vibrant colors from overwhelming the eye
- Use **elevated surface levels** (slightly lighter dark shades) to create hierarchy: background < card < tooltip
- Maintain **WCAG AA contrast ratios** (4.5:1 for text) -- test specifically in dark mode, as some color pairs pass on white but fail on dark
- Replace **light grey gridlines** with slightly lighter-than-background lines (e.g., #2A2A3E on #1A1A2E)
- Borders and separators should be **subtle** (1px, low-opacity white or lighter grey), not heavy dividers
- Test both **ambient light conditions**: dark mode in a dark room AND in daylight (outdoor mobile use)
- Use CSS custom properties / CSS variables to define **light and dark token sets** that swap cleanly

## Examples

### Good Practice
> [!tip] Do This
> - Ember's dark navy (#0D1B2A) as chart background with off-white text and muted-but-distinct series colors
> - Surface elevation: background #0D1B2A, card #1B2838, tooltip #253546 -- three clearly distinct levels
> - Charts that switch between light and dark mode via CSS variables with no JavaScript theme detection lag

### Bad Practice
> [!warning] Avoid This
> - Inverting a light-mode chart by simply setting `background: black` and `color: white` -- gridlines disappear, colors clash
> - Using fully saturated neon colors (lime green, hot pink) on dark backgrounds, causing eye strain in prolonged viewing
> - Dark mode where the chart area and its containing card are the same shade, making chart boundaries invisible

## Energy & Climate Applications
- Emission dashboards for control rooms: dark mode reduces eye strain during 12-hour monitoring shifts
- Presentation decks on projectors: dark background with high-contrast data elements projects well in conference rooms
- Real-time energy monitoring: dark mode with amber/green status indicators follows industrial SCADA conventions

## Applicable Chart Types
- [[Line Chart]] -- increase line thickness to 2.5-3px on dark backgrounds for visibility
- [[Bar Chart]] -- add subtle 1px lighter border to bars to separate them from the dark background
- [[Heatmap]] -- sequential palette must have sufficient lightness range to read cells against dark background
- [[KPI Card Array]] -- elevated card surfaces distinguish metrics from the page background
- [[Waterfall Chart]] -- connector lines need increased opacity on dark backgrounds
- [[Choropleth Map]] -- map borders should be a subtle lighter shade, not white outlines

## Tools & Implementation
- **CSS custom properties** -- define `--chart-bg`, `--chart-text`, `--chart-grid` tokens for light/dark swap
- **next-themes** -- Next.js theme provider with `ThemeProvider` for system-aware dark mode detection
- **Tailwind CSS `.dark` variant** -- class-based dark mode with `dark:bg-slate-900 dark:text-slate-100`

## Further Reading
- [Material Design Dark Theme Guide](https://material.io/design/color/dark-theme.html) -- Google's comprehensive dark mode design system
- [Apple Human Interface Guidelines: Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode) -- Apple's dark mode principles

## Related Principles
- [[Color for Data]]
- [[Accessibility in Dataviz]]
- [[Brand-Consistent Charts]]
- [[Emphasis and De-emphasis]]
