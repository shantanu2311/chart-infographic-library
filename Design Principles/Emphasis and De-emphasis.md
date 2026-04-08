---
title: Emphasis and De-emphasis
tags:
  - design-principle
  - emphasis
  - focus
  - visual-hierarchy
---

# Emphasis and De-emphasis

## The Principle
Not all data points are equally important. Emphasis directs the reader's attention to what matters most by making focal elements visually prominent and pushing context into the background. The most effective charts have a clear visual hierarchy: one element shouts, a few speak, and the rest whisper.

## Why It Matters
When everything is emphasized, nothing is. A chart where all bars are bright blue, all lines are the same weight, and all labels are the same size forces the reader to decide what matters -- and they often decide wrong or give up. Strategic emphasis reduces the reader's cognitive load and ensures the intended message lands.

## Key Guidelines
- Use **color saturation** as the primary emphasis tool: full saturation for the focal element, desaturated/grey for context
- **Grey out** context data rather than removing it -- context validates the focal point's significance
- Use **size contrast** to emphasize: thicker lines (3-4px vs 1px), larger points, bolder text for focal elements
- **Position matters**: the top-left quadrant gets the most attention in left-to-right reading cultures
- Apply **selective labeling**: label only the focal data point(s), not every single value
- In digital contexts, use **animation or motion** to draw the eye: a bar growing, a line drawing, a number counting up
- Use **whitespace** to isolate the focal element from surrounding context elements
- Combine at most **two emphasis channels** (e.g., color + size) to avoid creating visual noise

## Examples

### Good Practice
> [!tip] Do This
> - Highlighting solar's growth trajectory in vivid amber against all other energy sources in light grey
> - A scatter plot where one outlier facility is colored red and labeled, while all other facilities are small grey dots
> - A KPI card where the primary metric is 48px bold and the comparison metric is 14px regular grey text

### Bad Practice
> [!warning] Avoid This
> - A bar chart where every bar is a different bright color, creating a rainbow with no focal point
> - Bolding every axis label, annotation, and title equally so nothing stands out as primary
> - Adding drop shadows, glows, and borders to every element, creating visual noise instead of hierarchy

## Energy & Climate Applications
- Highlighting solar growth: vivid amber for solar against grey fossil fuel lines in an energy mix time series
- Emission hotspot identification: one facility's Scope 1 bar in red against grey bars for all other facilities
- Policy impact: bold the post-intervention period on a trend line while greying out the pre-intervention baseline

## Applicable Chart Types
- [[Line Chart]] -- thick colored focal line against thin grey context lines
- [[Bar Chart]] -- saturated focal bar(s) against grey context bars
- [[Scatter Plot]] -- larger colored focal points against small grey context points
- [[Area Chart]] -- focal source in full opacity, context sources at 20-30% opacity
- [[Small Multiples]] -- one highlighted panel in full color, rest greyed out
- [[Waterfall Chart]] -- largest contributing step in accent color, others in neutral grey
- [[KPI Card Array]] -- primary KPI in large bold type, secondary metrics smaller and lighter

## Tools & Implementation
- **CSS `opacity`** -- set context elements to 0.2-0.3 opacity while focal elements remain at 1.0
- **Recharts `Cell` component** -- conditionally color individual bars or points based on a highlight condition
- **Framer Motion `animate`** -- entrance animations that draw attention to focal elements on page load

## Further Reading
- [Preattentive Attributes (Stephen Few)](https://www.perceptualedge.com/articles/ie/visual_perception.pdf) -- the science of what the eye notices first
- [Storytelling with Data: Focus (Cole Nussbaumer Knaflic)](https://www.storytellingwithdata.com/blog/2017/7/26/focus) -- practical emphasis techniques

## Related Principles
- [[Color for Data]]
- [[Data-Ink Ratio]]
- [[Annotation Techniques]]
- [[Storytelling with Sequence]]
