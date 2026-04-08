---
title: Bar Chart
aliases:
  - Horizontal Bar Chart
tags:
  - chart-type/comparison
  - data-type/categorical
  - data-type/numeric
  - complexity/beginner
  - audience/general
  - audience/executive
  - audience/analyst
  - theme/energy-markets
  - theme/climate
  - theme/mdb
  - theme/renewable-energy
  - theme/public-finance
category: Comparison
complexity: beginner
best_audience: general, executive, analyst
---

# Bar Chart

## What It Is
A bar chart uses horizontal rectangular bars to represent data values, where the length of each bar is proportional to the value it represents. It is one of the most fundamental and universally understood chart types, ideal for comparing discrete categories. The horizontal orientation makes it particularly effective when category labels are long or numerous.

## Best Data Types
- Categorical data with a single numeric measure
- Ranked or sorted values across categories
- Named entities (countries, sectors, organisations) with associated quantities
- Survey results or frequency counts
- Budget allocations or funding breakdowns

## When to Use
- Comparing values across a moderate number of categories (5-30)
- When category labels are long text strings (country names, organisation names)
- Showing rankings or league tables
- Displaying results that benefit from easy left-to-right reading
- When the audience is broad and chart literacy varies
- Presenting part-to-whole comparisons when sorted by value

## When NOT to Use
> [!warning] Avoid When
> - You have continuous data along both axes (use a scatter plot instead)
> - You need to show trends over time (use a line chart or column chart)
> - You have only 2-3 categories (consider a simple table or big number display)
> - You have hundreds of categories (the chart becomes unreadable; filter or aggregate first)
> - You need to show relationships between two numeric variables

## Real-World Use Cases
- Revenue by product line in a quarterly business review
- Population by country in a UN demographic report
- Customer satisfaction scores across service categories
- Election results by candidate or party

### Energy & Climate Applications
- GHG emissions by sector (energy, industry, agriculture, transport, buildings) as reported in IEA World Energy Outlook
- Country-by-country comparison of installed renewable energy capacity (IRENA Renewable Capacity Statistics)
- MDB climate finance commitments by region (World Bank, ADB, AfDB, AIIB, EBRD) for a given fiscal year
- Fossil fuel subsidies by country from IEA or IMF estimates
- Carbon credit issuance volumes by registry (Verra, Gold Standard, ACR, CAR)

## Visual Style Variations
- **Sorted bar chart** — bars ordered by value descending for quick ranking identification
- **Grouped bar chart** — multiple bars per category for sub-group comparison (e.g., Scope 1/2/3 per country)
- **Diverging bar chart** — bars extending left and right from a central axis to show positive/negative deviations (e.g., above/below average emission intensity)
- **Highlighted bar chart** — one or two bars coloured differently to draw attention to a specific category (e.g., highlighting India among G20 nations)

## Related Charts
- [[Column Chart]] — vertical orientation of the same concept; better for time-based categories
- [[Lollipop Chart]] — reduces visual weight while conveying the same ranked comparison
- [[Dot Plot]] — strips away the bar entirely, useful when precision matters more than magnitude
- [[Bullet Chart]] — extends the bar with target markers and qualitative ranges

## Inspiration Sources
- [Data Viz Catalogue](https://datavizcatalogue.com/) — chart type reference
- [From Data to Viz](https://www.data-to-viz.com/) — decision tree
- [IEA Data Explorer](https://www.iea.org/data-and-statistics) — energy data visualisations using bar charts extensively
- [Our World in Data](https://ourworldindata.org/) — clear bar chart examples for emissions and energy
