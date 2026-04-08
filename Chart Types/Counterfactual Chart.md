---
title: Counterfactual Chart
aliases:
  - What-If Comparison Chart
  - Avoided Impact Chart
  - With-Without Chart
  - Scenario Delta Chart
tags:
  - chart-type/specialized
  - data-type/time-series
  - data-type/scenario
  - complexity/intermediate
  - audience/policymaker
  - audience/analyst
  - theme/renewable-energy
  - theme/climate
  - theme/energy-markets
  - theme/finance
category: Specialized
complexity: intermediate
best_audience: policymakers, analysts, advocates, journalists
---

# Counterfactual Chart

## What It Is
A visualization comparing what actually happened against what *would have happened* in the absence of a specific intervention, technology, or policy. The gap between the actual and counterfactual line represents the avoided impact. Ember uses this powerfully: "Without wind and solar added since 2019, the EU would have imported 92 billion m3 more gas and 55 million tonnes more coal, costing EUR 59 billion extra."

## Best Data Types
- Time series with an actual trajectory and a modelled counterfactual scenario
- Before/after intervention comparison where the "without" case must be estimated
- Avoided costs, avoided emissions, or avoided imports
- Policy impact assessment data

## When to Use
- Quantifying the value of a policy, technology, or investment that already happened
- Communicating "what we avoided" — making invisible benefits visible
- Comparing actual emissions trajectory with a business-as-usual counterfactual
- Justifying continued investment by showing cumulative avoided impact
- Showing the gap between "where we are" and "where we'd be without action"

## When NOT to Use
> [!warning] Avoid When
> - The counterfactual scenario is speculative and can't be robustly modelled
> - Multiple interventions overlap and individual attribution is unclear
> - The audience won't understand the hypothetical framing
> - Precise quantification matters more than narrative impact (use scenario comparison instead)
> - Cherry-picking the counterfactual to exaggerate impact

## Real-World Use Cases
- Medical trials: treatment group vs control group outcomes
- Economic policy: GDP with vs without stimulus package
- Infrastructure: travel time with vs without new transit line
- Insurance: losses with vs without risk mitigation measures

### Energy & Climate Applications
- **Ember's EU counterfactual**: Without wind+solar added since 2019, EU would have imported 92bn m3 more gas + 55Mt more coal, costing EUR 59 billion
- **Avoided emissions from renewables**: Total CO2 avoided globally by solar and wind vs fossil counterfactual
- **Carbon pricing impact**: Emissions trajectory with vs without EU ETS — quantifying the cap-and-trade effect
- **Energy efficiency gains**: Electricity demand with vs without efficiency improvements since 2000
- **Fossil fuel subsidy removal**: Modelled consumption with vs without subsidies
- **Paris Agreement assessment**: Projected warming with current NDCs vs without Paris Agreement (Climate Action Tracker)

## Visual Style Variations
- **Two-line comparison** — solid line (actual) vs dashed line (counterfactual), shaded gap between
- **Stacked area with "avoided" band** — actual trajectory as area, counterfactual as upper boundary, gap labeled
- **Waterfall bridge** — starting from counterfactual, showing avoided impact as a negative waterfall bar
- **Side-by-side bar** — actual vs counterfactual at a single point in time
- **Cumulative gap** — running total of the avoided impact growing over time

## Related Charts
- [[Area Chart]] — for shading the gap between actual and counterfactual
- [[Line Chart]] — base format for the two trajectories
- [[Waterfall Chart]] — for bridging between counterfactual and actual at a point in time
- [[Tornado Chart]] — for sensitivity analysis of counterfactual assumptions

## Tools That Support This
- Flourish (Ember's approach)
- D3.js (custom shaded area between lines)
- Datawrapper (annotation-rich line charts)
- ggplot2 (geom_ribbon for gap shading)

## Inspiration Sources
- [Ember — European Electricity Review 2025](https://ember-energy.org/latest-insights/european-electricity-review-2025/) — EUR 59bn avoided gas/coal import counterfactual
- [Climate Action Tracker — Warming Projections](https://climateactiontracker.org/global/temperatures/) — warming with vs without current policies
- [IEA — World Energy Outlook Scenarios](https://www.iea.org/reports/world-energy-outlook-2024) — STEPS vs NZE scenario comparison
