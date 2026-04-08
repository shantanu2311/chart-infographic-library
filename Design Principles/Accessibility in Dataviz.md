---
title: Accessibility in Dataviz
tags:
  - design-principle
  - accessibility
  - wcag
  - inclusive-design
---

# Accessibility in Dataviz

## The Principle
Accessible data visualization ensures that charts communicate effectively to all users, including those with color vision deficiency (8% of men, 0.5% of women), low vision, motor impairments, and users relying on screen readers. Accessibility is not an afterthought -- it is a design constraint that improves clarity for everyone.

## Why It Matters
An inaccessible chart excludes a significant portion of your audience. Colorblind users cannot distinguish red from green. Low-vision users cannot read 9px text. Screen reader users get nothing from an unlabeled SVG. Beyond ethics, accessibility is increasingly a legal requirement (WCAG 2.1 AA compliance). Every accessibility improvement -- higher contrast, clearer labels, larger targets -- also benefits the fully sighted.

## Key Guidelines
- Maintain **WCAG AA contrast ratios**: 4.5:1 for text, 3:1 for graphical elements against their background
- Avoid **red-green** as the sole differentiator; use blue-orange or blue-red diverging palettes instead
- Add **pattern fills** (hatching, dots, stripes) as a secondary channel alongside color in bar and area charts
- Write **meaningful alt text** for every chart: describe the key finding, not just "bar chart showing data"
- Structure charts in **semantic HTML** or SVG with proper ARIA roles (`role="img"`, `aria-label`)
- Ensure all interactive elements (tooltips, filters, legends) are **keyboard navigable** (Tab, Enter, Escape)
- Provide a **data table alternative** below or linked from every chart for screen reader users
- Use **sufficient line thickness** (2px minimum) and point sizes (6px minimum radius) for low-vision users

## Examples

### Good Practice
> [!tip] Do This
> - A stacked bar chart with both distinct colors AND pattern fills, plus a data table beneath for screen readers
> - Alt text: "Line chart showing India's grid emission factor declining 12% from 0.82 to 0.71 tCO2e/MWh between FY2020 and FY2025, with the steepest drop in FY2023"
> - Interactive legend items reachable via Tab key, toggling series via Enter, with visible focus indicators

### Bad Practice
> [!warning] Avoid This
> - A chart image with alt text "chart" or no alt text at all
> - Relying solely on thin colored lines (1px) against a white background with no labels or markers
> - Red slice = fossil, green slice = renewable with no text labels or patterns -- invisible to deuteranopia users

## Energy & Climate Applications
- Emission scope breakdown: use patterns (diagonal stripes for Scope 1, dots for Scope 2, crosshatch for Scope 3) alongside color
- Grid region comparison: include a sortable data table below the choropleth so users who cannot perceive the color scale can still access the ranking
- Dashboard KPIs: ensure sufficient contrast between the metric value and its background card in both light and dark mode

## Applicable Chart Types
- [[Bar Chart]] -- pattern fills + color, direct value labels, keyboard-navigable tooltips
- [[Line Chart]] -- distinct dash patterns per series, marker shapes at data points, thick lines
- [[Choropleth Map]] -- provide alternative ranked table; use sequential palette with sufficient lightness range
- [[Pie Chart]] -- direct labels with leader lines; patterns per slice; avoid relying on legend color matching
- [[Scatter Plot]] -- use distinct marker shapes (circle, square, triangle) alongside color for categories
- [[Heatmap]] -- add cell value labels; ensure sequential palette has sufficient contrast range

## Tools & Implementation
- **axe DevTools** -- automated accessibility audit for web-based charts and dashboards
- **Viz Palette** -- test categorical palettes against all types of color vision deficiency
- **Highcharts Accessibility Module** -- built-in screen reader support, keyboard navigation, and sonification

## Further Reading
- [Chartability](https://chartability.fizz.studio/) -- comprehensive accessibility audit methodology for data visualization
- [WCAG 2.1 Non-text Contrast (1.4.11)](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html) -- the specific success criterion for graphical elements

## Related Principles
- [[Color for Data]]
- [[Dark Mode Design]]
- [[Typography in Charts]]
- [[Mobile-Responsive Charts]]
