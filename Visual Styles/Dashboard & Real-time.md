---
title: Dashboard & Real-time
tags:
  - visual-style
  - dashboard
  - real-time
  - monitoring
  - trading
---

# Dashboard & Real-time

## What It Is
A high-density, multi-panel visual system designed for continuous monitoring and rapid decision-making. Every square centimeter of screen real estate carries information. Dark backgrounds reduce eye strain during extended viewing sessions. Neon and high-saturation accent colors draw attention to anomalies and alerts. The style assumes an expert user who does not need explanatory text — they need current state, trend direction, and threshold alerts at a glance. Latency matters: data should feel alive, not archived.

## Key Characteristics
- Dark background (near-black or deep navy) as the dominant canvas, reducing glare for 8+ hour viewing
- Multi-panel layout: 4-12 chart tiles arranged in a grid with consistent gutter spacing (8-12px)
- Compact typography — small font sizes (10-12px) with high contrast ratios against dark backgrounds
- Live-updating data with subtle pulse or glow animations on value changes
- Traffic-light severity system: green (normal), amber (warning), red (critical) with optional blue (info)
- Sparklines and mini-charts embedded within KPI cards for trend-at-a-glance context

## Color Palettes
- **Terminal Classic**: `#0a0a0a` (background), `#1a1a2e` (card surface), `#00ff88` (success/up), `#ff3366` (alert/down), `#4488ff` (info), `#ffaa00` (warning) — Bloomberg Terminal lineage
- **Grid Monitor**: `#0d1117` (GitHub dark), `#161b22` (elevated surface), `#58a6ff` (link/info), `#3fb950` (operational), `#f85149` (fault), `#d29922` (caution) — operations center
- **Energy Trading**: `#000814`, `#001d3d`, `#003566`, `#ffc300` (gold accent), `#e63946` (sell/alert), `#06d6a0` (buy/ok) — financial terminal aesthetic
- **Neon Ops**: `#0b0c10`, `#1b2838`, `#66fcf1` (cyan primary), `#45a29e` (muted cyan), `#c5c6c7` (text), `#fc4445` (critical) — cyberpunk operations vibe

## Typography
- **KPI Values**: Monospace or tabular — Fira Code, JetBrains Mono, or IBM Plex Mono at 24-36px, bold — numbers must align vertically across cards
- **Card Titles**: Sans-serif — Inter, Roboto, or Barlow at 12-14px, medium weight, uppercase or small-caps with letter-spacing
- **Axis Labels**: 9-10px, muted color (#888 on dark), consistent placement
- **Alert Text**: Same monospace at 11-12px, colored by severity level, sometimes with a colored left-border indicator
- **Timestamps**: 9px monospace, bottom-right of each panel, showing last-updated time

## Best For
- Energy trading floors monitoring spot prices, futures, and renewable generation forecasts
- Electricity grid control rooms tracking load, frequency, and renewable intermittency
- Carbon market live tracking — EU ETS, voluntary credits, compliance prices
- Real-time emissions monitoring for industrial facilities and fleet management
- NOC/SOC-style operational dashboards for energy infrastructure

### Energy & Climate Applications
- Live grid carbon intensity maps showing regional emission factors updating every 15 minutes
- Power plant performance dashboards with heat rate, capacity factor, and emission rate panels
- Carbon market trading screens with order book depth, price history, and volume indicators
- Fleet emissions monitoring for logistics companies tracking per-vehicle fuel consumption in real time

## Chart Types That Work Well
- [[Sparkline]] — ultra-compact trend indicators embedded in KPI cards; 24-hour or 7-day context at a glance
- [[Gauge / Radial]] — capacity utilization, emission thresholds, and target progress with color-coded zones
- [[Heatmap]] — time-of-day vs. day-of-week patterns for energy demand or grid carbon intensity
- [[Real-time Line Chart]] — streaming data with a moving window (15min, 1hr, 24hr); oldest data fades out
- [[Treemap]] — hierarchical breakdowns of emission sources or portfolio allocation in a space-efficient format

## Design Tips
> [!tip] Best Practices
> - Establish a clear visual hierarchy: primary KPIs at top or left, supporting detail charts below or right
> - Use animation sparingly and purposefully — a subtle pulse on value change is useful; continuous animation is distracting and drains GPU
> - Design for the "glance test": a user should identify the system state (healthy/warning/critical) within 2 seconds of looking at the dashboard
> - Maintain consistent time axes across all panels so the user can correlate events visually
> - Always show a "last updated" timestamp and a connection-status indicator; stale data on a real-time dashboard is worse than no data

## Tools & Software
- [[Grafana]] — open-source monitoring dashboards with built-in dark themes and real-time data source plugins
- [[Power BI]] — enterprise dashboards with streaming datasets and alert rules
- [[Tableau]] — real-time data connections with polished dark theme options
- Custom [[D3.js]] / [[React]] — full control for bespoke trading and monitoring interfaces

## Inspiration Sources
- [Bloomberg Terminal](https://www.bloomberg.com/professional/solution/bloomberg-terminal/) — the original dense, dark, data-saturated interface
- [Grafana Dashboards Gallery](https://grafana.com/grafana/dashboards/) — community-built monitoring dashboard examples
- [Electricity Maps](https://app.electricitymaps.com/) — live global grid carbon intensity visualization
- [WattTime](https://www.watttime.org/) — real-time marginal emissions data for grid optimization

## Related Styles
- [[Corporate & Business]]
- [[Dark Mode & High Contrast]]
- [[Data Journalism]]
