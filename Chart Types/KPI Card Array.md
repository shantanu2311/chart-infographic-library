---
title: KPI Card Array
aliases:
  - KPI Dashboard Cards
  - Metric Highlight Cards
  - Stat Cards
  - Big Number Cards
tags:
  - chart-type/kpi
  - data-type/numeric
  - data-type/categorical
  - complexity/beginner
  - audience/general
  - audience/business
  - audience/policymaker
  - theme/energy-markets
  - theme/climate
  - theme/renewable-energy
  - theme/finance
category: KPI
complexity: beginner
best_audience: general audiences, executives, policymakers, dashboard users
---

# KPI Card Array

## What It Is
A row of 3-5 large, prominent metric cards displayed as the hero element of a dashboard or report page. Each card shows a single key number with a label, optional trend indicator (arrow, sparkline, or percentage change), and sometimes a mini-chart. Ember uses this as the first thing users see on country profiles: three cards showing "22% low-carbon electricity", "10% solar+wind share", "78% fossil share."

## Best Data Types
- Single key performance indicators (KPIs)
- Headline metrics summarizing a larger dataset
- Percentage shares, absolute values, or change metrics
- Benchmark comparisons (actual vs target)

## When to Use
- As the hero element at the top of a dashboard or report page
- Providing immediate context before users dive into detailed charts
- Summarizing the "so what" of a complex analysis in 3-5 numbers
- Creating scannable executive summaries
- Country or entity profile pages where key stats orient the reader

## When NOT to Use
> [!warning] Avoid When
> - You need to show trends, distributions, or relationships (use proper charts)
> - There are more than 5-6 metrics (becomes overwhelming; prioritize)
> - The numbers need context that can't fit in a subtitle
> - The KPIs are not truly key — resist showing secondary metrics as KPIs

## Real-World Use Cases
- SaaS dashboards: MRR, churn rate, active users, conversion rate
- Financial dashboards: revenue, profit margin, cash position
- Operations: uptime %, response time, ticket volume

### Energy & Climate Applications
- **Ember country profiles**: 3 cards — low-carbon share %, solar+wind share %, fossil share %
- **Carbon market dashboard**: EUA price, VCM issuance volume, global coverage %
- **Renewable energy summary**: installed capacity (GW), LCOE ($/MWh), investment ($bn), capacity factor (%)
- **GHG inventory hero**: total emissions (MtCO2e), intensity (tCO2e/unit), year-over-year change (%)
- **ESG report header**: ESG score, carbon footprint, renewable energy %, water intensity

## Visual Style Variations
- **Number + label** — simplest: large number, small descriptor underneath
- **Number + trend arrow** — green up/red down arrow with % change
- **Number + sparkline** — mini line chart inside the card showing recent trend
- **Number + progress ring** — circular progress indicator around the number
- **Number + comparison** — "22% (vs 18% last year)" dual-value format
- **Traffic light** — green/amber/red background indicating performance status

## Related Charts
- [[Gauge Chart]] — single-metric dial, more visual but takes more space
- [[Sparkline]] — the inline trend often embedded within KPI cards
- [[Bullet Chart]] — for KPIs that need actual-vs-target context
- [[Waffle Chart]] — for percentage KPIs that benefit from visual proportion

## Tools That Support This
- Any dashboard tool (Tableau, PowerBI, Grafana, Metabase)
- Flourish (Ember's choice)
- Custom HTML/CSS (most flexible)
- Figma (for design mockups)

## Inspiration Sources
- [Ember Country Profiles](https://ember-energy.org/countries-and-regions/india/) — 3-card KPI hero pattern
- [Carbon Tracker Dashboard](https://carbontracker.org/) — climate finance KPI cards
- [Bloomberg Terminal](https://www.bloomberg.com/professional/) — financial KPI card arrays
