---
layout: lesson
title: COVID-19 Spatial Clustering I
purpose: "practice reproducing a prior study"
format: workshop
term: sp25
---

## Goals and Expectations

**Before Class**

- Based on reading alone, draw a workflow diagram representing your best guess at Chakraborty's research design. You will need a digital version of the workflow for inclusion in your repository, whether drawn digitally or scanned.
- I suggest printing the article or using Zotero to highlight three types of clues with three colors:
  - Data sources and characteristics thereof
  - Methods and analysis
  - Intermediary and final results that could be compared with a reproduction study
- It is unlikley that you will be familiar with all of the methods. At this stage, it is OK to document a method as one "step" in analysis and take notes on *context clues* about how that method works.

**During Class**

- Create a reproducible compendium for reproducing the study and add data provided by the author.
- Draft an analysis plan as an *orgininal study* for implementing the study up to the point of defining *clusters* to be used in GEE (generalized estimating equation) models.
- Convert the analysis plan into a *reproduction study*, including the purpose of the reproduction study, any planned devations from the prior study and methods for comparing results
- Knit the analysis plan to html 
- Update the project `readme.md` and `LICENSE` files, and documentation of `procedure_index.csv`, `data_index.csv`, and `data/metadata`.
- Create a version `release` of your compendium on GitHub prior to analyzing any data and commit a version of the repository prior to analyzing data.

## Reading

- Chakraborty, J. 2021. Social inequities in the distribution of COVID-19: An intra-categorical analysis of people with disabilities in the U.S. *Disability and Health Journal* 14 (1):101007. DOI: [10.1016/j.dhjo.2020.101007](https://doi.org/10.1016/j.dhjo.2020.101007).

## Resources

- Use [Draw.io](https://draw.io) to draw a workflow diagram representing your understanding of the research design, or draw neatly by hand or with a tablet.

### Kulldorff spatial scan statistics

- [SaTScan](https://www.satscan.org) software for spatial scan statistics, including a [user guide](https://www.satscan.org/cgi-bin/satscan/register.pl/SaTScan_Users_Guide.pdf)
- [SpatialEpi Package](https://cran.r-project.org/package=SpatialEpi) R package for spatial epidemiology, and its [GitHub Repository](https://github.com/rudeboybert/SpatialEpi) and [reference manual](https://cran.r-project.org/web/packages/SpatialEpi/SpatialEpi.pdf)
- [R Data and Methods for Spatial Epidemiology: the SpatialEpi Package](https://faculty.washington.edu/jonno/SISMIDmaterial/SpatialEpiVignette.pdf)

### Relative Risk

- CDC DSEPD Principles of Epidemiology in Public Health Lesson 3: [Measures of Risk](https://archive.cdc.gov/#/details?url=https://www.cdc.gov/csels/dsepd/ss1978/lesson3/section5.html)

### Generalized Estimating Equations

- University of Virginia Library [GEE Introduction](https://data.library.virginia.edu/getting-started-with-generalized-estimating-equations/)
- [gee Package](https://cran.r-project.org/web/packages/gee/index.html) and [reference manual](https://cran.r-project.org/web/packages/geepack/vignettes/geepack-manual.pdf)
- [The R Package geepack for Generalized Estimating Equations](file:///C:/Users/josephh/AppData/Local/Temp/v15i02.pdf) academic paper by the package authors, Halekoh, Højsgaard, and Yan