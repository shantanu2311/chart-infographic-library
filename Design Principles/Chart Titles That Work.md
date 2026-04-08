---
title: Chart Titles That Work
tags:
  - design-principle
  - titles
  - narrative
  - editorial
---

# Chart Titles That Work

## The Principle
A chart title is the single most-read element on any visualization. It frames what the reader should take away before they even look at the data. The best titles are declarative -- they state the finding, not just the topic. The subtitle then provides scope, methodology, and source attribution.

## Why It Matters
A descriptive title like "Electricity Generation by Source" forces the reader to analyze the chart themselves to find the story. A declarative title like "Solar surpassed coal for the first time in 2024" tells them the story immediately, then the chart provides the evidence. Research shows declarative titles increase reader comprehension and recall by 25-30%.

## Key Guidelines
- Write **declarative titles** that state the key finding for analytical and editorial contexts
- Use **descriptive titles** only for exploratory dashboards where the reader is meant to find their own story
- Add a **subtitle** for scope (geography, time range), units, and data source: "India | FY2020-2025 | Source: CEA v21.0"
- Place the title **top-left aligned** (not centered) to match Western reading patterns; left edge anchors the eye
- Keep titles to **one line** on desktop; two lines maximum on mobile
- Use **present tense** for current states ("Solar leads...") and past tense for historical findings ("Emissions peaked in...")
- Include the **magnitude or direction** of the finding: "up 42%", "halved since 2015", "surpassed X"
- Avoid starting with articles ("The", "A") -- start with the subject: "India's steel sector..." not "The steel sector of India..."

## Examples

### Good Practice
> [!tip] Do This
> - Declarative: "India's grid became 12% cleaner in five years" with subtitle "Grid emission factor, tCO2e/MWh | FY2020-FY2025 | Source: CEA"
> - Milestone-driven (Ember style): "Renewables generated more electricity than coal in October 2024"
> - Dashboard descriptive: "Scope 1 Emissions by Fuel Type" with subtitle "Select a facility to filter | FY2024-25"

### Bad Practice
> [!warning] Avoid This
> - Vague: "Emissions Data" -- says nothing about what the reader should see
> - Too long: "A Comprehensive Analysis of Greenhouse Gas Emissions Across Multiple Industrial Facilities in the Northern Grid Region of India for the Financial Year 2024-2025"
> - Missing source: any chart title without attribution to a data source, especially in reports or publications

## Energy & Climate Applications
- Ember's report titles as model: milestone-focused, specific, with the takeaway embedded: "Wind and solar generated a record 30% of global electricity in 2023"
- Policy charts: "EAF steelmakers can cut emissions 48% with three proven technologies" -- actionable finding as title
- BRSR reporting: "Scope 2 emissions fell 15% after solar PPA" -- compliance narrative with clear cause-effect

## Applicable Chart Types
- [[Line Chart]] -- trend titles: "X rose/fell by Y% between A and B"
- [[Bar Chart]] -- comparison titles: "Solar capacity additions outpaced all other sources in FY2024"
- [[Waterfall Chart]] -- decomposition titles: "Three factors drove the 22% emission reduction"
- [[Pie Chart]] -- composition titles: "Electricity accounts for 63% of total Scope 2 emissions"
- [[Area Chart]] -- shift titles: "Renewable share doubled while coal retreated to 55%"
- [[Scatter Plot]] -- relationship titles: "Larger facilities show lower emission intensity per tonne"

## Tools & Implementation
- **Headline testing** -- write 3 title variants and test with a colleague; the clearest one wins
- **Datawrapper title field** -- enforces title + description + source fields as mandatory chart metadata
- **Recharts `<text>` elements** -- position custom title and subtitle SVG text with precise alignment

## Further Reading
- [How to Write Better Chart Titles (Datawrapper)](https://blog.datawrapper.de/chart-titles/) -- practical guide with before/after examples
- [Storytelling with Data: Titles](https://www.storytellingwithdata.com/blog/2017/3/22/so-what) -- "So what?" test for every chart title

## Related Principles
- [[Annotation Techniques]]
- [[Storytelling with Sequence]]
- [[Typography in Charts]]
