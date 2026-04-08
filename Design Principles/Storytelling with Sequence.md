---
title: Storytelling with Sequence
tags:
  - design-principle
  - storytelling
  - narrative
  - scrollytelling
---

# Storytelling with Sequence

## The Principle
Data storytelling uses a deliberate sequence of charts to build a narrative arc: context, complication, resolution. Rather than showing one complex chart with everything, progressive disclosure walks the reader from simple foundations to complex insights, each chart building on the previous one.

## Why It Matters
A single chart with 8 series, 3 annotations, and a dual axis overwhelms the reader. The same data presented as a sequence of 4 simpler charts -- each adding one layer of complexity -- is absorbed effortlessly. Narrative sequence leverages how humans naturally process information: setup, tension, payoff. This is how the best data journalism (FT, NYT, Ember) structures its analysis.

## Key Guidelines
- Start with **the simplest view** that establishes context: a single line, one bar chart, or a headline number
- **Add complexity incrementally**: introduce new series, breakdowns, or annotations one at a time
- Use **before/after reveals**: show the baseline chart, then overlay the change or intervention
- Structure in **chapters**: Ember's report pattern of overview -> deep dive -> regional -> outlook
- Apply **scrollytelling** for web: sticky chart that transforms as the reader scrolls through narrative text
- Use **consistent visual encoding** throughout the sequence so the reader doesn't re-learn the chart at each step
- End with a **synthesis or call-to-action** chart that brings together the insights from the sequence
- Pace the sequence: **3-5 charts** for a focused story, **8-12 charts** for a full report chapter

## Examples

### Good Practice
> [!tip] Do This
> - Step 1: Total global emissions (one line, 1990-2024). Step 2: Split into fossil + renewable (two lines). Step 3: Add country breakdown (small multiples). Step 4: Highlight India's trajectory with annotation.
> - Before/after: show a facility's emission profile pre-retrofit, then animate the change to post-retrofit on the same axes
> - Scrollytelling: a fixed area chart that progressively highlights each energy source as the reader scrolls through explanatory paragraphs

### Bad Practice
> [!warning] Avoid This
> - Dumping 12 charts on a single page with no narrative thread connecting them -- just a data gallery
> - Showing the complex final chart first, then "zooming in" to simpler views -- this reverses the natural learning order
> - Inconsistent encoding: using blue for solar in chart 1 and yellow for solar in chart 3

## Energy & Climate Applications
- COP submission narratives: open with national total, drill into sectors, spotlight the policy-relevant sector, end with reduction pathway
- Ember's Global Electricity Review: macro trend -> record milestones -> regional deep dives -> forward-looking scenarios
- MSME audit report: facility overview -> scope breakdown -> hotspot identification -> recommended interventions -> projected impact

## Applicable Chart Types
- [[Line Chart]] -- foundational for time-series narrative progression
- [[Area Chart]] -- composition stories that build from total to breakdown
- [[Waterfall Chart]] -- decomposition stories: start with total, reveal the contributing factors
- [[Small Multiples]] -- the "comparison chapter" in a sequence showing patterns across categories
- [[Bar Chart]] -- ranking or comparison chapters within the broader narrative
- [[Sankey Diagram]] -- flow stories: where energy/emissions come from and where they go

## Tools & Implementation
- **Scrollama** (JS library) -- intersection observer-based scrollytelling for sticky chart + scrolling narrative
- **Flourish Stories** -- no-code sequential chart presentations with transitions between slides
- **Reveal.js + chart libraries** -- presentation framework for live-updating charts that build slide by slide

## Further Reading
- [Storytelling with Data (Cole Nussbaumer Knaflic)](https://www.storytellingwithdata.com/) -- the definitive guide to narrative data visualization
- [The Pudding](https://pudding.cool/) -- exemplary scrollytelling with progressive data revelation

## Related Principles
- [[Chart Titles That Work]]
- [[Annotation Techniques]]
- [[Chart Animation Guidelines]]
- [[Emphasis and De-emphasis]]
