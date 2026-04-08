---
title: NYT Graphics
tags:
  - source-organization
  - journalism
  - data-journalism
  - scrollytelling
  - gold-standard
---

# NYT Graphics

## Overview
The New York Times graphics department is widely regarded as the gold standard of data journalism visualization. With a team of 50+ visual journalists, developers, and designers, they produce work that ranges from daily news charts to ambitious interactive investigations. Their annotation-driven approach and mastery of D3.js have defined modern data storytelling for the digital era.

## Signature Visual Style
- **Color palette**: Restrained and deliberate. Light backgrounds (#F7F7F7), NYT grey tones for secondary elements. Selective emphasis with a single highlight color — often a warm amber, teal, or red depending on story. Never more than 3-4 colors per chart
- **Typography**: NYT's proprietary typefaces (NYT Cheltenham for headlines, NYT Franklin for body). Strong serif/sans-serif contrast. Direct labels preferred over legends
- **Layout**: Narrative-first — text and charts interleaved in scrollytelling format. Charts sized to fill viewport at key moments, then shrink to margin position as narrative continues
- **Tone**: Investigative, explanatory, meticulous. Every pixel earns its place

## Strengths
- Annotation-driven storytelling: charts are narrated, not just displayed, with precise callouts
- Mastery of [[Scrollytelling]] format with smooth transitions between narrative states
- Extensive use of [[Direct Labeling]] eliminating the need for legends entirely
- Custom SVG illustrations blended seamlessly with data visualization
- Willingness to invent novel chart forms when standard types cannot tell the story

## Chart Types They Favor
- [[Line Chart]] — heavily annotated with direct labels, callout boxes, and reference events marked on the axis
- [[Scatter Plot]] — relationship stories with selective labeling of notable outliers and trend annotations
- [[Choropleth Map]] — geographic stories with bivariate encoding and carefully designed map projections
- [[Small Multiples]] — comparing patterns across dozens of entities in tight grid layout
- [[Custom SVG]] — bespoke visual forms created for specific stories (e.g., connected dot plots, slope charts, bump charts)

## Design Patterns Worth Studying
- **Scrollytelling mastery**: Charts that transform through 5-10 narrative states, each triggered by scroll position, building understanding incrementally
- **Annotation-driven narrative**: Every chart has 3-5 precise annotations pointing the reader to the key findings, eliminating ambiguity about what to see
- **Minimal color with selective emphasis**: Grey for context, one color for the story — forcing the reader's eye to the data that matters
- **Direct labeling over legends**: Data series labeled inline next to the relevant line or bar, never in a separate legend box

## Energy & Climate Relevance
The NYT produces landmark climate visualizations including temperature anomaly maps, emissions tracking, extreme weather attribution, and energy transition coverage. Their climate desk combines data journalism with investigative reporting, producing stories that shape public understanding of climate change. Their "how much hotter" personalized climate tools are benchmarks for engagement.

## Key Reports / Products
- **Climate section** — Ongoing data-driven coverage of global warming, extreme weather, and energy policy
- **The Upshot** — Data-focused section combining charts with analysis on policy and economics
- **Interactive investigations** — Long-form scrollytelling pieces (election needles, COVID trackers, climate projections)
- **Daily news charts** — Static and interactive charts accompanying daily reporting
- **D3.js contributions** — Mike Bostock (NYT alumnus) created D3.js; the team continues to push its boundaries

## Data Access
- Interactive graphics viewable with NYT subscription (soft paywall)
- No raw data downloads in most cases
- Occasional GitHub repositories shared for notable methodologies
- D3.js (open source) created by former NYT team members
- Source citations included linking to underlying datasets

## Related Sources
- [[Reuters Graphics]]
- [[The Economist]]
- [[The Pudding]]
- [[FiveThirtyEight]]
