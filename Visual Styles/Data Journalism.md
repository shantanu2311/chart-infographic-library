---
title: Data Journalism
tags:
  - visual-style
  - journalism
  - annotation
  - evidence
  - analysis
---

# Data Journalism

## What It Is
An evidence-first visual methodology where the chart is not decoration but the core argument. Every annotation earns its place by explaining a data point the reader would otherwise miss. The style sits between editorial restraint and storytelling energy — more structured than a Pudding essay, more alive than a policy brief. The journalist's job is to find the story hiding in the data and surface it through strategic visual emphasis, contextual annotations, and carefully chosen chart forms. The reader leaves understanding not just what happened, but why it matters.

## Key Characteristics
- Annotation-heavy: callout lines, labeled inflection points, contextual notes directly on the chart surface
- Neutral base palette with strategic color highlights — grey for context, color for the story
- Multiple chart types within a single piece, each chosen to answer a specific question
- Source transparency: methodology notes, data provenance, uncertainty ranges shown explicitly
- Responsive design with mobile-specific chart layouts (not just scaled-down desktop versions)
- Headline as thesis statement: the title tells you the finding, the chart proves it

## Color Palettes
- **FiveThirtyEight Neutral**: `#f0f0f0` (background), `#999999` (context lines), `#ff6600` (highlight), `#3a86a6` (secondary), `#333333` (text) — the annotation-first palette
- **Reuters Clarity**: `#ffffff` (clean white), `#b0b0b0` (grid), `#d63031` (alert red), `#0984e3` (trust blue), `#2d3436` (text) — institutional credibility
- **NYT Upshot**: `#f7f7f7` (off-white), `#cccccc` (muted grid), `#e15759` (red), `#4e79a7` (blue), `#59a14f` (green) — Tableau-derived, proven in newsrooms
- **Climate Specific**: `#ffffcc` to `#800026` (sequential heat), `#2166ac` to `#b2182b` (diverging blue-red) — warming stripes and anomaly maps

## Typography
- **Headlines**: Strong sans — Franklin Gothic, Barlow Condensed, or Atlas Grotesk at 24-32px, bold — states the finding
- **Deck/Subtitle**: Regular weight, 16-18px, one sentence expanding on the headline
- **Body/Annotations**: Clean sans — Roboto, Source Sans, or Noto Sans at 13-15px, regular, for inline chart annotations
- **Axis Labels**: 11-12px, medium grey (#666), uppercase for units (e.g., "MILLION TONNES CO2e")
- **Source Line**: 9-10px, light grey, bottom-left: "Source: IEA World Energy Outlook 2025 | Chart: [Author]"

## Best For
- Carbon market analysis and price movement stories with annotated context
- Energy transition storytelling — tracking renewable capacity growth against policy milestones
- Climate attribution reporting linking emissions data to observable impacts
- Election-style "tracker" formats applied to national climate targets (NDCs) and their progress
- Investigative pieces exposing gaps between pledged and actual emissions reductions

### Energy & Climate Applications
- Annotated emissions trajectory charts showing where policies kicked in (or failed to)
- India's grid decarbonization story with CEA data, annotated with coal plant retirements and solar additions
- Carbon credit price analysis with event annotations (policy announcements, market shocks)
- Facility-level emission intensity comparisons across steel plants with sector benchmark overlays

## Chart Types That Work Well
- [[Annotated Line Chart]] — the workhorse of data journalism; trend + context annotations make the story self-contained
- [[Dot Plot / Strip Plot]] — distribution comparison across categories without the abstraction of box plots; each point is meaningful
- [[Small Multiples]] — same chart repeated across categories for pattern comparison; lets the reader discover the story
- [[Bump Chart]] — ranking changes over time; which countries or sectors are rising/falling in emissions league tables
- [[Diverging Bar Chart]] — above/below a baseline; perfect for showing which sectors exceeded or met reduction targets

## Design Tips
> [!tip] Best Practices
> - Write annotations as mini-headlines: "Coal generation peaked here in 2024" not "Note: this is the maximum value"
> - Use grey (#cccccc) for all context data and reserve your single highlight color for the subject of the story
> - Show uncertainty explicitly — confidence intervals, ranges, or "estimated" labels — because credibility depends on honesty about what the data does not tell us
> - Build mobile layouts separately, not responsively: a complex annotated desktop chart often needs a completely different form factor on a phone screen
> - Always include a "How we did this" methodology note, even if brief; it is the difference between journalism and marketing

## Tools & Software
- [[D3.js]] — the gold standard for bespoke, annotation-rich, responsive data journalism graphics
- [[ai2html]] — Adobe Illustrator to responsive HTML; used by NYT, WSJ, and Reuters for production graphics
- [[Datawrapper]] — fast, responsive, annotation-friendly; the newsroom daily driver for standard chart types
- [[R]] / [[ggplot2]] — analysis and publication-quality static charts; the `ggrepel` and `ggannotate` packages add annotation power

## Inspiration Sources
- [FiveThirtyEight](https://fivethirtyeight.com/) — pioneered the annotation-heavy, evidence-forward chart style
- [Reuters Graphics](https://graphics.reuters.com/) — exemplary interactive data journalism across climate and energy
- [NYT The Upshot](https://www.nytimes.com/section/upshot) — analytical journalism with chart-as-argument methodology
- [Carbon Brief](https://www.carbonbrief.org/) — climate-specific data journalism with deep annotation practice

## Related Styles
- [[Minimal & Editorial]]
- [[Playful & Storytelling]]
- [[Dashboard & Real-time]]
