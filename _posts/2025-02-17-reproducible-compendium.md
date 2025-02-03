---
layout: lesson
title: Reproducible Geographic Research
purpose: "practice reproducible geographic research with R and a research compendium"
format: workshop
term: sp25
---

## Reading

1. Nüst, D., and E. Pebesma. 2021. Practical Reproducibility in Geography and Geosciences. *Annals of the American Association of Geographers* 111 (5):1300–1310. DOI:[10.1080/24694452.2020.1806028](https://doi.org/10.1080/24694452.2020.1806028).

## Application

1. Discuss and study how to use a [template for reproducible research](https://github.com/HEGSRR/HEGSRR-Template)

## References

1. Ibanez, L., W. J. Schroeder, and M. D. Hanwell. 2014. Practicing open science. In Implementing Reproducible Research, eds. V. Stodden, F. Leisch, and R. D. Peng, 241–280. Boca Raton: CRC Press.
2. Millman, K. J., and F. Perez. 2014. Developing Open-Source Scientific Practice. In Implementing Reproducible Research, eds. V. Stodden, F. Leisch, and R. D. Peng, 149–183. Boca Raton: CRC Press.
3. Nüst, D., C. Boettiger, and B. Marwick. 2018. How to Read a Research Compendium. arXiv:[1806.09525](http://arxiv.org/abs/1806.09525).
4. Wilson, J. P., K. Butler, S. Gao, Y. Hu, W. Li, and D. J. Wright. 2021. A Five-Star Guide for Achieving Replicability and Reproducibility When Working with GIS Software and Algorithms. *Annals of the American Association of Geographers* 111 (5):1311–1317. DOI:[10.1080/24694452.2020.1806026](https://doi.org/10.1080/24694452.2020.1806026).

## Resources

1. Nüst and others are developing infrastructure for containerized executable compendia at [o2r.info/](https://o2r.info/)
1. Docker containers allow researchers to reproduce and share their research processing environments as virtual machines which can be run on a server. [www.docker.com/](https://www.docker.com/)

## Tutorial

- Video Tutorial Orientation to Reproducible Geographic Research with Github and R
  - [normalized audio levels](https://midd.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx?folderID=0d30511e-30a1-4e22-a82a-b082011f114a)
  - [non-normalized audio levels](https://midd.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx?folderID=a4152bea-fe8a-4695-95fa-b0840116ec51)
- [R for Geospatial Processing workshop](https://bakaniko.github.io/FOSS4G2019_Geoprocessing_with_R_workshop/) presented by Nicolas Roelandt in Bucharest, Romania. Here's the [repository](https://github.com/Bakaniko/FOSS4G2019_Geoprocessing_with_R_workshop)
  - Disregard the `cartography` package and section 5.5 of the workshop. We can do everything we need to do with `tmap`. If you're interested in the more advanced print cartography package for R, you can try cartography's successor: `mapsf` <https://riatelab.github.io/mapsf/>

## Software

- Base R: [R project for statistical computing](https://www.r-project.org/)
- RStudio: [posit downloads](https://posit.co/downloads/)
- GitHub: [Desktop Application](https://desktop.github.com/)

## Essential packages

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
- [Geocomputation with R](https://r.geocompx.org/)
- [Spatial Data Science](https://rspatial.org)
- [Introduction to R for Geospatial Data](https://datacarpentry.org/r-intro-geospatial/)
- [Introduction to Geospatial Raster and Vector Data with R](https://datacarpentry.org/r-raster-vector-geospatial/)