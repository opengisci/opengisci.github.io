---
layout: lesson
title: "Generalized Estimating Equations and motivations for open science"
purpose: "understand how generalized estimating equations work and discuss motivations for open GIScience"
format: lecture
date: 2023-09-28 11:15
term: fa23
---

## Readings

1. Hanley, J. A., Negassa, A., Edwardes, M. D. de B., & Forrester, J. E. (2003). Statistical analysis of correlated data using generalized estimating equations: An orientation. American Journal of Epidemiology, 157(4), 364–375. https://doi.org/10.1093/aje/kwf215

## Resources

1. Rmarkdown walkthrough of the analysis in Hanley et al (2003): [Learn-GEE](https://github.com/opengisci/Learn-GEE)

## Save for future date
1. choice of papers with further context and motivation for open GIScience
  - Nelson, T. A., Goodchild, M. F., & Wright, D. J. (2022). Accelerating ethics, empathy, and equity in geographic information science. Proceedings of the National Academy of Sciences of the United States of America, 119(19). https://doi.org/10.1073/pnas.2119967119
  - Rey, S. J. (2022). Big Code. Geographical Analysis, 1–14. https://doi.org/10.1111/gean.12330

## Key Ideas and Concepts

- Correlation statistics may be based on normal continuous data (Parametric), using Pearson's *R*, or based on ordinal ranked data (Nonparametric) using Spearman's *Rho*. The resulting *R* or *Rho* range from `-1` to `1` where:
  -`-1` is perfect inverse correlation
  - `0` is no correlation
  - `1` is perfect positive correlation
- Linear models consist of:
  - dependent variable
  - independent variables
  - constant / intercept
  - coefficients
  - estimated values
  - residuals / errors
  - standard error
  - 95% confidence intervals
- While linear models assume that each observation is independent, spatial autocorrelation violates this assumption.
- GEE approaches the autocorrelation problem by
  - defining clusters
  - assuming that correlation can be expected *within* clusters, but that clusters are *independent* of one another
  - estimating correlation within clusters
  - weighting observations based on correlation within clusters and cluster size
  - with no correlation within clusters, weights still equal `1`
  - with perfect correlation within clusters, weights approach `1/k` where `k` is the cluster size