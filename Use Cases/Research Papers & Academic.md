---
title: Research Papers & Academic
tags:
  - use-case
  - academic
  - research
  - peer-review
  - scientific
---

# Research Papers & Academic

## Overview
Research papers and academic publications demand visualizations that meet the highest standards of scientific rigor, reproducibility, and methodological transparency. Figures must survive peer review, render correctly in both digital and print formats, and communicate complex statistical relationships to expert audiences. Journal-specific formatting requirements often constrain design choices significantly.

## Audience
- Peer reviewers evaluating methodology and results for publication decisions
- Fellow researchers in climate science, energy economics, and sustainability fields
- Graduate students studying literature and replicating methodologies
- Conference attendees viewing poster presentations and slide decks
- Policymakers and practitioners referencing academic evidence for decision-making

## Key Requirements
- Full reproducibility with documented data sources, processing steps, and visualization code
- Grayscale-friendly designs that remain legible in black-and-white journal print editions
- Compliance with journal figure guidelines (DPI, font sizes, panel labeling, file formats)
- Statistical precision with proper axis labels, units, significance indicators, and error representations
- Compact multi-panel layouts that maximize information per figure allowance

## Recommended Chart Types
- [[Scatter Plot]] — Displaying correlations, regression results, and outlier identification with confidence intervals
- [[Box Plot]] — Summarizing distributions across experimental conditions or model scenarios with quartile detail
- [[Violin Plot]] — Combining distribution shape with summary statistics for richer comparison across groups
- [[Line Chart]] — Time-series analysis with multiple model outputs, confidence bands, and observed vs. predicted overlays
- [[Histogram]] — Frequency distributions of model residuals, measurement uncertainty, or Monte Carlo simulation outputs

## Recommended Visual Styles
- [[Minimal]] — Maximizing data-ink ratio per Tufte principles, removing all non-essential visual elements for clarity
- [[Corporate]] — Structured, professional formatting that meets institutional and journal publication standards

## Recommended Infographic Formats
- [[Statistical Infographic]] — Multi-panel figure layouts combining related analyses (regression, residuals, sensitivity) in a single figure
- [[Comparison Infographic]] — Model intercomparison layouts showing multiple approaches applied to the same dataset

## Example Outputs
- Nature Climate Change research article figures with multi-panel regression and sensitivity analysis
- Energy Policy journal charts comparing policy effectiveness across countries with statistical testing
- NBER working paper figures presenting econometric results with robustness checks
- IPCC AR6 Working Group technical figures synthesizing hundreds of studies into assessed ranges
- Conference poster visualizations optimized for A0 printing with hierarchical reading flow

### Energy & Climate Examples
- Climate model ensemble spread plots showing CMIP6 projections with observed temperature overlays
- Marginal abatement cost curve (MACC) comparing mitigation options by cost-effectiveness and potential
- Energy technology learning rate scatter plots with log-log regression and prediction intervals
- Spatial autocorrelation analysis of renewable energy deployment with Moran's I visualization
- Multi-model comparison of integrated assessment model (IAM) emission pathways with uncertainty fans

## Tools & Platforms
- R (ggplot2) with publication themes (theme_classic, cowplot) for reproducible, journal-ready figures
- Python (matplotlib, seaborn) with style sheets matching journal requirements and LaTeX integration
- LaTeX (TikZ/pgfplots) for figures directly embedded in manuscript source with consistent typography
- Julia (Makie.jl) for high-performance scientific visualization with GPU-accelerated rendering

## Design Tips
> [!tip] Best Practices
> - Use shape and pattern differentiation in addition to color so figures work in grayscale printing
> - Label panels consistently (a, b, c or i, ii, iii) and reference them explicitly in the manuscript text
> - Include sample sizes (n=) directly on figures rather than only in captions or text
> - Export at minimum 300 DPI for raster graphics; prefer vector formats (SVG, PDF, EPS) when possible
> - Provide figure source code and data in supplementary materials or a public repository for reproducibility

## Common Mistakes
> [!warning] Avoid These
> - Using color as the sole differentiator between categories, making figures inaccessible in grayscale
> - Omitting units on axes or using ambiguous abbreviations without a legend definition
> - Presenting model outputs without uncertainty quantification (confidence intervals, prediction bands, p-values)
> - Exceeding journal figure count limits by not combining related analyses into well-designed multi-panel figures

## Related Use Cases
- [[Policy Briefs & COP Submissions]]
- [[Energy Sector Reports]]
- [[Education & Training]]
