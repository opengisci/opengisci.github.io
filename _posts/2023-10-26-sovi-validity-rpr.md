---
layout: lesson
title: SoVI Validity Reproduction and Reanalysis
purpose: "reproduce and reanalyze Spielman et al's replication of SoVI"
format: lab
date: 2023-10-26 13:30
term: fa23
---

Reproduce Spielman et al.'s replication of the SoVI and validity checks.

The reproduction study can be found here: <https://github.com/HEGSRR/RPl-Spielman-2020>

A discussion thread about the study can be found [here](https://github.com/opengisci/FA23/discussions/4) 

Let's all attempt a common *reanalysis* strategy for this paper. 
We will adjust the SoVI construction to *weight* the SoVI components by the percentage of variance they explain.

## Instructions

1. Work in small groups with at least one python expert in each group
2. Set up an Anaconda python environment with python version 3.9.18
3. Install JupyterHub to that python environment
4. Fork and Clone the <https://github.com/HEGSRR/RPl-Spielman-2020> responsitory
5. Run and edit the Rpr2-Spielman-2020 notebook
6. Map national SoVI with the Folium package for slippy maps. Hint: you need a key_on value for a unique ID, and this can be 'feature.properties.GEOID' to use the `GEOID` field
7. Create an output table of factor loadings for national SoVI. These are stored in the `weights_rot` table of PCA output
8. Calculate and output the percent variance explained by each component of the national SoVI. This is typically the eigenvalue of a component divided by the sum of all eigenvalues. Eigenvalues are the same as the sum of squared loadings. In this case, percent variance can be calculated as `sum_sq_load_rot / sum(eigenvals_all)`
9. Reweight the SoVI by the percentage variance explained of each component, rather than using a simple sum of the components. The bulk of this should happen around steps M5-M8. 
10. After running all of the code, export your notebook as an `html` file and save to the `docs` folder
11. Update your website with blog & links to the study.

## Update

Reweighting required adjustments to code throughout the study. To be fair to the intent of the study, both the loadings and the SoVI scores needed to be weighted. I think I have implemented this correctly throughout the repository as a new notebook, `Rpl-Spielman-Weighted.ipynb` which generates a new set of output data, tables, and figure.
