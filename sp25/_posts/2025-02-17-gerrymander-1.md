---
layout: lesson
title: Gerrymandering I
purpose: "practice reproducible geographic research with a research compendium"
format: workshop
term: sp25
---

## Goals and Expectations

- Create a reproducible research compendium
- Plan a study to measure districting fairness in the context of gerrymandering
- Knit the analysis plan to `html` format and save to the `docs` folder
- Update the project `readme.md` and `LICENSE` files, and documentation of `procedure_index.csv`, `data_index.csv`, and `data/metadata`.
- Create a version `release` of your compendium on GitHub prior to analyzing any data  
- Based on what you know of the reproducibility crisis and/or your own geographic research projects, post a short blog about the relative value or burden of starting a project with a compendium and analysis plan.
- Start implementing the study using R

## Tutorial Application

In this tutorial, we will get an introduction to practicing open science by:

- Creating a reproducible research compendium from a GitHub [template for reproducible research](https://github.com/HEGSRR/HEGSRR-Template)
- Using RStudio and R
- Planning and implementing a gerrymandering study [papers for context](https://drive.google.com/open?id=1WPLbx69EhKRK4LGD9MrZD7bMrF2u9v4b&usp=drive_fs) and [data for Alabama](https://drive.google.com/open?id=1HUFgFcngZBW8Lf0xv_1giY9DSnD4tb6u&usp=drive_fs)
- Reproducible R code for downloading and manipulating spatial data
- Learning vignette for [Simple Features in R](https://opengisci.github.io/Learn-Simple-Features/) *updated with guidance on Geodesic area and perimeter calculations
- Starter example [research compendium](https://github.com/josephholler/OR-Gerrymander-Alabama)
- How to [release a version](https://midd.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=e5db0d9d-8d7e-40e3-999d-b2890155a3c6)

## Software

- Base R: [R project for statistical computing](https://www.r-project.org/)
- RStudio: [posit downloads](https://posit.co/downloads/)
- GitHub: [Desktop Application](https://desktop.github.com/)

## R packages for reproducible spatial analysis

- [groundhog](https://groundhogr.com/) for reproducible computational environments (consistent versions of R and its packages)
- [here](https://here.r-lib.org/) for reproducible path names
- [tidyverse](https://www.tidyverse.org/) includes [dplyr](https://dplyr.tidyverse.org/) for database-style data frames
- [sf](https://r-spatial.github.io/sf/) provides support for spatial vector data implementing the OSGeo *simple features*  standards we are accustomed to
- [stars](https://r-spatial.github.io/stars/) spatial-temporal raster data in R
- [tmap](https://r-tmap.github.io/tmap/) thematic maps, including static maps or interactive leaflet maps

### Alternative packages

- [sp](https://cran.r-project.org/web/packages/sp) alternative package for spatial vector data
- [raster](https://cran.r-project.org/web/packages/raster) alternative raster data package
- [mapsf](https://riatelab.github.io/mapsf/) alternative for static map cartography mapsf [presentation slides with vignettes](https://rcarto.github.io/user2021)

## Other Tutorial Resources

- [R Markdown Code Chunks](https://rmarkdown.rstudio.com/lesson-3.html)
- [Spatial Data Science With applications in R](https://r-spatial.org/book/) by Pebesma and Bivand
- [Geocomputation with R](https://r.geocompx.org/)
- [Spatial Data Science](https://rspatial.org)
- [Introduction to R for Geospatial Data](https://datacarpentry.org/r-intro-geospatial/)
- [Introduction to Geospatial Raster and Vector Data with R](https://datacarpentry.org/r-raster-vector-geospatial/)

## References

1. Nüst, D., and E. Pebesma. 2021. Practical Reproducibility in Geography and Geosciences. *Annals of the American Association of Geographers* 111 (5):1300–1310. DOI:[10.1080/24694452.2020.1806028](https://doi.org/10.1080/24694452.2020.1806028).
2. Wilson, J. P., K. Butler, S. Gao, Y. Hu, W. Li, and D. J. Wright. 2021. A Five-Star Guide for Achieving Replicability and Reproducibility When Working with GIS Software and Algorithms. *Annals of the American Association of Geographers* 111 (5):1311–1317. DOI:[10.1080/24694452.2020.1806026](https://doi.org/10.1080/24694452.2020.1806026).
3. Ibanez, L., W. J. Schroeder, and M. D. Hanwell. 2014. Practicing open science. In Implementing Reproducible Research, eds. V. Stodden, F. Leisch, and R. D. Peng, 241–280. Boca Raton: CRC Press.
4. Millman, K. J., and F. Perez. 2014. Developing Open-Source Scientific Practice. In Implementing Reproducible Research, eds. V. Stodden, F. Leisch, and R. D. Peng, 149–183. Boca Raton: CRC Press.
5. Nüst, D., C. Boettiger, and B. Marwick. 2018. How to Read a Research Compendium. arXiv:[1806.09525](http://arxiv.org/abs/1806.09525).

### Other templates and tools

1. Nüst and others are developing infrastructure for containerized executable compendia at [o2r.info/](https://o2r.info/)
2. Docker containers allow researchers to reproduce and share their research processing environments as virtual machines which can be run on a server. [www.docker.com/](https://www.docker.com/)
3. Carl Boettiger's [research template](https://github.com/cboettig/template)
4. WORCS Workflow for Open Reproducible Code in Science [R Package](https://cjvanlissa.github.io/worcs/)
5. Project TIER [Protocol 4.0](https://www.projecttier.org/tier-protocol/protocol-4-0/)