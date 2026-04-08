---
title: Journalism & Editorial
tags:
  - use-case
  - journalism
  - editorial
  - data-storytelling
  - narrative
---

# Journalism & Editorial

## Overview
Journalism and editorial visualizations serve the public through news articles, investigative reports, and data-driven stories about climate, energy, and sustainability. These must balance analytical rigor with narrative accessibility, guiding readers through complex topics with annotated, contextual, and often interactive graphics. The best examples become reference points in public discourse.

## Audience
- General public consuming news through web and print media
- Engaged readers following climate and energy policy developments
- Other journalists and editors seeking data for their own reporting
- Researchers and advocates monitoring media framing of climate issues
- Students and educators using journalism as teaching material

## Key Requirements
- Narrative-driven design that supports the story arc rather than existing in isolation
- Heavy annotation with contextual labels, callouts, and explanatory text within the chart
- Accessibility for readers with no domain expertise in climate science or energy systems
- Responsive design adapting from desktop longform to mobile vertical scrolling
- Fast loading with progressive enhancement for interactive elements

## Recommended Chart Types
- [[Line Chart]] — Annotated time-series showing temperature records, emissions trends, or energy prices with event markers
- [[Scatter Plot]] — Revealing relationships (GDP vs. emissions, renewable investment vs. deployment) with labeled outliers
- [[Choropleth Map]] — Geographic storytelling about climate impacts, policy variation, or resource distribution across regions
- [[Bump Chart]] — Showing rank changes over time (country emissions rankings, energy source dominance shifts)
- [[Area Chart]] — Cumulative narratives (total emissions since industrial revolution, growing renewable share)

## Recommended Visual Styles
- [[Data Journalism]] — Purpose-built for storytelling with integrated annotations, step-by-step reveals, and editorial color choices
- [[Minimal]] — Clean, distraction-free layouts that let the data narrative carry the reader without decorative interference

## Recommended Infographic Formats
- [[Timeline Infographic]] — Historical narratives (evolution of climate policy, energy transition milestones, disaster chronology)
- [[Interactive Infographic]] — Scrollytelling experiences that reveal data progressively as the reader moves through the story

## Example Outputs
- Guardian climate coverage with annotated warming stripe banners and embedded interactive charts
- Reuters Graphics deep-dive visual essays on energy transition economics
- New York Times climate section feature with scrollytelling temperature and sea-level data
- The Pudding interactive explorations making abstract climate data tangible and personal
- FiveThirtyEight-style analysis combining statistical modeling with accessible chart annotation

### Energy & Climate Examples
- Annotated CO2 concentration timeline from Keeling Curve with historical event markers
- Interactive electricity generation map showing hourly fuel mix by country with playback
- Investigative scatter plot exposing gap between corporate net-zero pledges and actual emissions trajectories
- Bump chart of top 20 emitting countries showing rank changes from 1990 to present
- Scrollytelling piece on Arctic sea ice extent decline with seasonal animation and satellite imagery

## Tools & Platforms
- D3.js for bespoke interactive graphics with full editorial control over every element
- Scrollama or GSAP ScrollTrigger for scroll-driven narrative visualization experiences
- Datawrapper for rapid, accessible, responsive charts with built-in annotation tools
- ai2html (Adobe Illustrator to HTML) for pixel-perfect responsive editorial graphics

## Design Tips
> [!tip] Best Practices
> - Annotate directly on the chart surface; do not rely on legends that force the reader to look away from the data
> - Use a "read it in 10 seconds, study it in 2 minutes" layered design with headline, key insight, then detail
> - Provide context for every number: "X tonnes of CO2 is equivalent to Y cars driven for a year"
> - Build mobile-first and test on actual devices; most news consumption happens on phones
> - Use animation purposefully to show change over time, not for decoration

## Common Mistakes
> [!warning] Avoid These
> - Creating standalone charts that make sense in isolation but fail to connect to the article's narrative
> - Using interactive features that are invisible or broken on mobile devices
> - Presenting data without human context (raw gigatonnes mean nothing without relatable comparisons)
> - Truncating axes or manipulating scales to exaggerate trends, which erodes reader trust

## Related Use Cases
- [[Social Media & Advocacy]]
- [[Education & Training]]
- [[Research Papers & Academic]]
