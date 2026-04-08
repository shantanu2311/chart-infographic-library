---
title: Dark Mode & High Contrast
tags:
  - visual-style
  - dark-mode
  - accessibility
  - high-contrast
  - presentation
---

# Dark Mode & High Contrast

## What It Is
A design approach built around dark backgrounds and carefully calibrated high-contrast data colors that optimize for two things simultaneously: visual impact and perceptual accessibility. This is not simply "invert the colors" — it requires rethinking every design decision from color selection to typography weight to shadow direction. Done well, data pops off a dark canvas with cinematic intensity. Done poorly, it creates eye strain, illegible text, and invisible chart elements. The style commands attention in dim environments — conference halls, trading floors, evening presentations — and communicates technical sophistication.

## Key Characteristics
- Dark background as primary canvas: true black (`#000000`) for OLED or near-black (`#0d1117`, `#1a1a2e`) for reduced halation
- WCAG AAA contrast ratios (7:1 minimum) for all text and critical data elements against the dark surface
- Vibrant but not neon data colors — saturated enough to read on dark, desaturated enough to avoid afterimage
- Reduced use of pure white (`#ffffff`) for text; prefer off-white (`#e6e6e6`, `#d4d4d4`) to reduce glare
- Subtle elevation through lighter surface colors (not shadows, which are invisible on dark backgrounds)
- Careful treatment of chart gridlines: very low opacity (`#333333` to `#444444`) to provide structure without noise

## Color Palettes
- **Accessible Spectrum**: `#121212` (background), `#1e1e1e` (surface), `#bb86fc` (purple), `#03dac6` (teal), `#cf6679` (error pink), `#e0e0e0` (text) — Material Dark inspired, WCAG compliant
- **Energy Monitor**: `#0a0e17` (deep navy), `#162032` (card), `#22d3ee` (cyan data), `#f59e0b` (amber data), `#ef4444` (red alert), `#d1d5db` (text) — grid monitoring aesthetic
- **Carbon Dark**: `#0c0c0c`, `#1c1c1c` (surface), `#10b981` (emerald green), `#f472b6` (pink), `#60a5fa` (blue), `#fbbf24` (gold), `#f5f5f5` (text) — sustainability dashboard
- **Presentation Mode**: `#000000` (true black for projection), `#2a2a2a` (card), `#ffffff` (headline text), `#ff6b6b` (accent 1), `#4ecdc4` (accent 2), `#ffe66d` (accent 3) — maximum stage impact

## Typography
- **Headlines**: Medium to bold weight sans-serif — Inter, Outfit, or Plus Jakarta Sans at 28-40px in off-white (`#e8e8e8`)
- **Body**: Regular weight at 14-16px in light grey (`#b0b0b0` to `#d0d0d0`) — pure white body text causes eye fatigue on dark backgrounds
- **Data Values**: Semibold or bold in the data series color at 12-14px — color-coding values matches them to their chart elements
- **Axis/Grid Labels**: 10-12px in muted grey (`#777777` to `#999999`), just visible enough to provide context
- **Key Rule**: Increase font weight by one step compared to light-mode equivalents — thin fonts disappear on dark backgrounds

## Best For
- Conference presentations and keynote slides in dim auditoriums
- Digital dashboards displayed on wall-mounted screens in operations centers
- Evening [[COP]] sessions and side event presentations
- Energy trading screens and financial terminal interfaces
- Mobile applications where OLED true-black saves battery and looks premium

### Energy & Climate Applications
- Live emission monitoring dashboards for industrial facilities displayed on control room screens
- Carbon market trading interfaces where price movements need instant visual parsing
- Renewable energy generation dashboards shown on lobby displays at solar/wind farms
- Climate model output visualizations for researcher workstations during long analysis sessions

## Chart Types That Work Well
- [[Heatmap]] — vibrant color gradients on dark backgrounds create striking intensity maps; temperature anomalies and grid demand patterns
- [[Radar / Spider Chart]] — glowing lines on dark canvas feel like instrument readouts; multi-axis performance comparison
- [[Candlestick Chart]] — green/red candles on black are the universal language of trading interfaces
- [[Network Graph]] — nodes and edges with glow effects on dark backgrounds create compelling system topology views
- [[Gradient Area Chart]] — semi-transparent gradient fills from colored line to dark background; elegant emission trend visualization

## Design Tips
> [!tip] Best Practices
> - Never just invert a light-mode design — dark mode requires its own color palette, contrast testing, and spacing adjustments
> - Test all colors with a contrast checker: aim for 7:1 (AAA) for body text, 4.5:1 (AA) minimum for large text and data elements
> - Use color pairs that are distinguishable by colorblind users: avoid red/green as the only differentiator; use blue/orange or purple/yellow as alternatives
> - Add a subtle 1px border or 2-4% lighter background to cards and panels to define edges — without shadows, dark-on-dark elements merge invisibly
> - Avoid pure saturated colors (`#ff0000`, `#00ff00`) as data series colors; they cause afterimage and are harsh on dark backgrounds — shift toward muted tones (`#ef4444`, `#22c55e`)

## Tools & Software
- [[Figma]] — dark mode component libraries and contrast plugins (Stark, A11y) for design-time validation
- [[Grafana]] — native dark theme with extensive customization for monitoring dashboards
- [[Recharts]] / [[D3.js]] — full programmatic control over dark-mode chart theming in React and vanilla JS
- [[Tailwind CSS]] — `dark:` variant utilities make implementing and maintaining dark mode systematic

## Inspiration Sources
- [Bloomberg Terminal](https://www.bloomberg.com/professional/) — decades of dark-mode data density refinement
- [Electricity Maps](https://app.electricitymaps.com/) — dark-mode global grid visualization with excellent color choices
- [Material Design Dark Theme Guidelines](https://m3.material.io/styles/color/dark-theme) — Google's systematic approach to dark mode
- [Apple Human Interface Guidelines - Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode) — platform-level dark mode best practices

## Related Styles
- [[Dashboard & Real-time]]
- [[Corporate & Business]]
- [[Minimal & Editorial]]
