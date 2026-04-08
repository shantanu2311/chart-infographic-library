# Chart & Infographic Library

A comprehensive, open-source reference library for data visualization — built as an [Obsidian](https://obsidian.md/) vault with 116 interlinked notes covering **60 chart types, 31 data contexts, 8 infographic styles, 8 visual styles, and 8 use cases**.

Focused on **energy markets, climate change, finance, sustainability, and the global energy transition**.

> Built with [Claude Code](https://claude.ai/claude-code) by Anthropic.

---

## What's Inside

| Folder | Notes | What It Covers |
|---|---|---|
| **Chart Types** | 60 | Every major chart type from bar charts to Sankey diagrams, plus novel types like S-Curve Growth Charts, Counterfactual Charts, and Threshold Trackers |
| **Data Contexts** | 31 | Domain-specific guides: Carbon Markets, Hydrogen Economy, ESG, Loss & Damage, Article 6, Ember Global Electricity Data, and more |
| **Infographic Styles** | 8 | Statistical, Timeline, Process, Comparison, Geographic, Hierarchical, List, Interactive |
| **Visual Styles** | 8 | Minimal & Editorial, Corporate, Handwritten, Playful, Data Journalism, Dashboard, Poster, Dark Mode |
| **Use Cases** | 8 | Policy Briefs, Investor Decks, Energy Reports, Social Media, Education, Business Dashboards, Journalism, Academic |
| **Index** | 1 | Master index with chart selection table, purpose-based recommendations, and curated inspiration sources |

---

## Chart Types (60)

### Comparison
Bar, Column, Lollipop, Bullet, Dot Plot, Dumbbell, Radar, Tornado, Quadrant, Radial Bar

### Distribution
Histogram, Box Plot, Violin Plot, Density Plot, Ridgeline Plot, Population Pyramid

### Composition (Part-to-Whole)
Pie, Donut, Treemap, Sunburst, Waffle, Stacked Bar, Marimekko, Pictogram, Nightingale Rose

### Hierarchical
Packed Circle Chart

### Relationship
Scatter Plot, Bubble, Heatmap, Correlogram, Network Diagram, Parallel Coordinates, Connected Scatter Plot

### Flow
Sankey Diagram, Alluvial Diagram, Chord Diagram, Funnel

### Temporal
Line, Area, Stream Graph, Bump, Candlestick, Gantt, Racing Bar, Sparkline, S-Curve Growth, Seasonal Pattern

### Geospatial
Choropleth Map, Cartogram, Bubble Map, Tile Map

### KPI & Dashboard
Gauge, Combo Chart, KPI Card Array

### Design Patterns
Small Multiples

### Specialized
Waterfall, Slope, Change Attribution, Counterfactual, Threshold Tracker

---

## Data Contexts (31)

### Core Energy & Climate
Energy Markets, Climate & Emissions, Carbon Markets, Renewable Energy & Transition, Net Zero Pathways, COP UNFCCC IEA

### Finance & Economics
Financial Markets, Public Finance & MDBs, ESG & Sustainable Finance, Green Bonds & Climate Finance, Blended Finance, Loss & Damage Finance

### Technology & Infrastructure
Hydrogen Economy, Electric Vehicles & E-Mobility, Grid Infrastructure & Energy Storage, Carbon Capture & Storage (CCS/CCUS), Nuclear Energy, Climate Tech & Cleantech Startups

### Environment & Nature
Biodiversity & Nature-Based Solutions, Deforestation & Land Use Change, Circular Economy & Waste, Methane & Non-CO2 Emissions

### Policy & Governance
Climate Disclosure & TCFD/ISSB, Article 6 & International Carbon Trading, Just Transition & Social Impact, Climate Adaptation & Resilience, Climate Risk & Insurance

### Broader Intersections
Geopolitics & Energy Security, Commodity Markets (Oil Gas Metals), Supply Chain & Critical Minerals

### Reference
Ember Global Electricity Data (complete design system, color palette, data tools, API reference)

---

## Every Chart Note Includes

- **What It Is** — clear 2-3 sentence definition
- **Best Data Types** — what kind of data works
- **When to Use** — ideal situations
- **When NOT to Use** — common pitfalls (Obsidian callout format)
- **Real-World Use Cases** — general + energy/climate/finance-specific examples
- **Energy & Climate Applications** — 3-5 domain-specific examples referencing IEA, UNFCCC, Ember, carbon markets, MDBs, etc.
- **Visual Style Variations** — different ways to render the chart
- **Related Charts** — `[[wikilinks]]` to related types with rationale
- **Inspiration Sources** — curated links to reference sites

---

## How to Use

### As an Obsidian Vault
1. Clone this repo into your Obsidian vault directory
2. Open Obsidian and select the folder as a vault (or add it to an existing vault)
3. Explore via the **Index.md** or use **Graph View** to see all connections
4. Use tags in the search panel to filter by `chart-type/`, `data-type/`, `complexity/`, `audience/`, or `theme/`

### As a Reference
Browse the markdown files directly on GitHub. Each note is self-contained and readable without Obsidian.

---

## Tagging System

| Tag Namespace | Examples |
|---|---|
| `chart-type/` | `comparison`, `distribution`, `composition`, `relationship`, `flow`, `temporal`, `geospatial`, `specialized` |
| `data-type/` | `categorical`, `continuous`, `time-series`, `geographic`, `hierarchical`, `relational`, `financial`, `emissions`, `energy` |
| `complexity/` | `beginner`, `intermediate`, `advanced` |
| `audience/` | `general`, `business`, `analyst`, `researcher`, `designer`, `policymaker` |
| `theme/` | `energy-markets`, `climate`, `finance`, `carbon-markets`, `renewable-energy`, `net-zero`, `supply-chain`, `critical-minerals`, `mdb`, `cop-unfccc`, `iea`, `public-finance` |

---

## Chart Selection Quick Reference

| Purpose | Recommended Charts |
|---|---|
| Compare values | Bar, Column, Bullet, Dot Plot, Tornado |
| Show trends | Line, Area, Bump, Sparkline |
| Show distribution | Histogram, Box Plot, Violin, Ridgeline, Population Pyramid |
| Show composition | Pie, Treemap, Stacked Bar, Waffle, Pictogram |
| Show relationships | Scatter, Bubble, Heatmap, Correlogram, Parallel Coordinates |
| Show flows | Sankey, Alluvial, Chord |
| Show geographic | Choropleth, Bubble Map, Cartogram, Tile Map |
| Show change | Waterfall, Slope, Dumbbell, Racing Bar |
| Show rankings | Bump, Lollipop, Bar, Racing Bar |
| Show hierarchy | Treemap, Sunburst, Packed Circle |
| KPI / dashboard | Gauge, Combo, Sparkline, Small Multiples, KPI Card Array |
| Financial data | Candlestick, Line, Waterfall |
| Seasonal analysis | Seasonal Pattern, Heatmap, Radial Bar |
| Track adoption | S-Curve Growth, Threshold Tracker, Line |
| Explain drivers | Change Attribution, Waterfall, Tornado |
| Show avoided impact | Counterfactual, Waterfall, Area |

---

## Inspiration Sources

### Beautiful Examples
- [Information is Beautiful](https://informationisbeautiful.net/) — David McCandless
- [The Pudding](https://pudding.cool/) — interactive data journalism
- [Our World in Data](https://ourworldindata.org/) — comprehensive metrics
- [Storytelling with Data](https://www.storytellingwithdata.com/) — narrative approach
- [The Economist Graphic Detail](https://www.economist.com/graphic-detail)
- [Datawrapper River](https://app.datawrapper.de/river/) — community charts

### Chart Type Catalogs
- [DataViz Project](https://datavizproject.com/) — every chart type cataloged
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [Data Viz Catalogue](https://datavizcatalogue.com/) — charts by function
- [Chartopedia by AnyChart](https://www.anychart.com/chartopedia/) — encyclopedia
- [Visual Vocabulary by FT](https://ft-interactive.github.io/visual-vocabulary/)

### AI-Powered Chart Tools
- [Powerdrill Bloom](https://powerdrill.ai/bloom) — multi-agent AI chart recommendations
- [Infogram](https://infogram.com) — 35+ types, 800+ maps
- [Napkin AI](https://napkin.ai) — text-to-visual generation
- [Canva + Flourish](https://canva.com) — Magic Charts, scrollytelling

### Energy & Climate Data
- [Ember Electricity Data Explorer](https://ember-energy.org/data/electricity-data-explorer/) — 215 countries, open data
- [IEA Data & Statistics](https://www.iea.org/data-and-statistics)
- [IRENA Data & Statistics](https://www.irena.org/Data)

---

## Stats

- **116 notes** total
- **1,332 wikilinks** cross-referencing between notes
- **72 unique tags** spanning chart type, data type, complexity, audience, and theme
- **9,501 lines** of content
- Every chart note has a dedicated **Energy & Climate Applications** section

---

## License

This work is open source. Use it, fork it, adapt it for your domain.

---

## Contributing

Suggestions for new chart types, data contexts, or corrections are welcome. Open an issue or submit a pull request.

---

*Built with [Claude Code](https://claude.ai/claude-code) by Anthropic.*
