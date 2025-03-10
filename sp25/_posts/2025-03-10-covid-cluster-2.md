---
layout: lesson
title: COVID-19 Spatial Clustering II
purpose: "practice reproducing a prior study"
format: workshop
term: sp25
---

## Goals and Expectations

- Implement your analysis plan using R
- Discuss your results and conclude the study
- Knit the study report to `html` format and save to the `docs` folder 
- Use what you learn from Kedron and Holler (2024) and Schmitt (1978) to frame your goals and interpret your findings
- Update the project `readme.md` file, `procedure_index.csv`, `data_index.csv`, and `data/metadata` documentation.
- Create a version `release` of your compendium on GitHub once the analysis is complete and the report is rendered
- Write a blog post to highlight your findings using the validity readings and link to the report
- Mid-semester self-evaluation

## Reading

- Kedron, P. and Holler, J. (2024).  Validation and Verification of Applied GIS Research. *The Geographic Information Science & Technology Body of Knowledge (2024 Edition)*, John P. Wilson (ed.). DOI: [10.22224/gistbok/2024.1.13](https://doi.org/10.22224/gistbok/2024.1.13)
- Schmitt, R. R. (1978). Threats to validity involving geographic space. *Socio-Economic Planning Sciences*, *12*(4), 191–195. DOI: [10.1016/0038-0121(78)90044-7](https://doi.org/10.1016/0038-0121(78)90044-7)

## Implementation Suggestions

- Don't worry about calculating *p-values* or significance levels. Given the large sample size, these are not very meaningful anyway.
- You may learn from any of the code in `01-Rpr-Chakraborty.Rmd`, but follow your own plan of analysis (i.e. don't necessarily follow all of the deviations in that analysis). The code can work with a groundhog date of `2025-02-01`, with the exception that maps should be made with the new `tmap` package. 
- If two dataframes (matricies) have the same number of rows and columns, you can subract one from the other to compare
- Remember the `st_drop_geometry()` function for converting a geographic dataframe into a normal dataframe
- Expect the `kulldorff` function to take a long time to run.
- The `kulldorff` function takes a long time to run and produces a result in a complex data structure consisting of one `most.likely.cluster` and a long list of `secondary.clusters`. Each of these in turn has a list of `location.IDs.included`: a list of fips codes for the counties included in the cluster. If we have a data object `covid_kulldorff` with the results of our `kulldorf` function, we can get the FIPS codes of the counties in the most likely cluster with `covid_kulldorff$most.likely.cluster$location.IDs.included`.
- When interpreting Kulldorff results and differences between software, it may be helpful to distinguish between options that can be selected by the researcher in software vs decisions that are encoded in software, without any straightforward way to alter them.
- You may explore given data layers in QGIS, and use `st_write()` to export geopackages to view outputs in QGIS.

### Reference

- Longley, P. A., M. F. Goodchild, D. J. Maguire, and D. W. Rhind. 2008. Geographical information systems and science 2nd ed. Chichester: Wiley.
  - Chapter 6: *Uncertainty*, (pages 127-153)


