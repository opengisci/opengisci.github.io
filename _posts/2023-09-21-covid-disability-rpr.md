---
layout: lesson
title: "Disability and COVID-19 Reproduction"
purpose: "reproduce county-level association of disability and COVID-19"
format: lab
date: 2023-09-21 13:30
term: fa23
---

The purpose of this workshop is to reproduce Chakraborty (2021) and in doing so, learn about spatial scan statistics for epidemiology and about generalized estimating equations.

Chakraborty, J. 2021. Social inequities in the distribution of COVID-19: An intra-categorical analysis of people with disabilities in the U.S. *Disability and Health Journal* 14 (1):101007. DOI: [10.1016/j.dhjo.2020.101007](https://doi.org/10.1016/j.dhjo.2020.101007).

## Procedure

- **fork** the [HEGSRR/RPr-Chakraborty-2021](https://github.com/HEGSRR/RPr-Chakraborty-2021) repository to your own GitHub account
- **clone** the repository to your local machine
- **execute** the analysis
- **document** changes to your understanding of the research design by amending your workflow diagram
- **comment** any potential errors, uncertainties, or opportunities for improvement
- **compare** results to the original publication
- **draft** thoughts highlighting what you have *learned from* this reproduction study so far and *identifying* any errors, uncertain decisions, or opportunities for improving the study design or its reproducibility

## API: Application Program Interface

This analysis makes use of the Census API.
An API is an interface for passing data or commands between different software programs ([Wikipedia](https://en.wikipedia.org/wiki/API)).
Examples of APIs in spatial data science include:

- [DHS Surveys](https://api.dhsprogram.com)
- [Census](https://www.census.gov/data/developers/data-sets.html)
- [OpenStreetMap Overpass](https://wiki.openstreetmap.org/wiki/Overpass_API)
- [QGIS](https://qgis.org/api/3.10/)
- [GRASS](https://grasswiki.osgeo.org/wiki/GRASS_GIS_APIs)
- [Twitter](https://developer.twitter.com/en/docs/twitter-api)
- [Google Earth Engine](https://r-spatial.github.io/rgee/)

If an API is useful for data science, it is very common to find packages facilitating connection to the API from Python or R.

- [rdhs](https://cran.r-project.org/package=rdhs)
- [tidycensus](https://cran.r-project.org/package=tidycensus)
- [osmdata](https://cran.r-project.org/web/packages/rgrass7/index.html)
- [rtweet](https://cran.rstudio.com/package=rtweet)
- [rqgis](https://github.com/r-spatial/RQGIS)
- [rgrass7](https://cran.r-project.org/web/packages/rgrass7/index.html)

Additionally, if a data course is useful for data science, it's common to find an R package specific to loading that data source. For example:

- [GADMTools](https://cran.r-project.org/package=GADMTools) for [GADM](https://gadm.org/)
- [rnaturalearth](https://cran.r-project.org/package=rnaturalearth) for [Natural Earth](https://www.naturalearthdata.com/)
