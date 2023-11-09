---
layout: lesson
title: COVID-19 Spatial Accessibility Preanalysis
purpose: "plan reanalysis or replication of COVID-19 spatial accessibility"
format: lecture
date: 2023-11-09 11:15
term: fa23
---

## Prepare for lecture

Brainstorm ways in which the research compendium for this notebook could be improved, including revisions to:

- fix errors
- reduce uncertainty
- improve reproducibility
- improve visualization of results

We will collaborate in an in-person class discussion to more deeply understand the Python script for this analysis and identify opportunities for improving and extending its functionality, especially to more completely implement the analysis in the published research paper.

## Results from spring 2021

The Spring 2021 lecture concluded with a challenge: what is the largest source of error in the current version of the python Jupyter notebook?
We determined the answer to be *boundary effects* introduced to the analysis when the geographic extent was limited to Chicago.
The road network was limited to boundaries for Chicago that exclude Midway Airport, while population data was limited to boundaries for Chicago including the airport, and hospitals were included within a buffer distance of Chicago.
The inconsistent spatial extents caused the Midway Airport area to seem inaccessible to health care, and caused hospitals in the buffer outside of Chicago to snap to the nearest node of the road network without accounting for the distance between the hospital and the boundary of Chicago.
Finally, services outside of Chicago were included but population demand on those services was not.

### Spring 2021 class questions and ideas for reanalysis

- [ ] There are other models besides two-step catchment analysis for spatial interaction in health geography, e.g. gravity model.
- [ ] How important or efficient is the network simplification function? Does this impact the locations/connectivity of any hospitals?
- [ ] Clarify use of packages and functions throughout the code
- [ ] Could area-weighted reaggregation be used for the overlap analysis?
- [ ] Why are hexagons used for the analysis as opposed to other spatial data structures, e.g. a raster-like tessellation of squares? In other words, is there a modifiable areal unit problem? Does the use of different sizes and shapes for the unit of analysis matter?
- [ ] How are weights justified for the enhanced distance bands? Would different weights significantly change outcomes?
- [ ] For reproducibility, we should filter hospital types in the code, rather than beforehand.
- [ ] Should the default network speed be set to 35mph?
- [ ] Could other forms of transit be included? Why is the analysis dependent upon personal vehicle use?
- [ ] Is there a better indicator for hospital capacity other than ventilators or ICU Beds?
- [ ] Pay attention to CRSs: are they always transformed when they need to be? Can the final maps be projected?
- [ ]  Add time benchmark to key sections of code with `%%time` as the first line of the code block
