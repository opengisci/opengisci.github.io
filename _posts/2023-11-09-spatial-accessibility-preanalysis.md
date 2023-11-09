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

- [x] Fix boundary / edge effects stemming from limited extent of road network and need to expand analysis beyond city of Chicago for accurate results within the city. **Done** by including a buffered road network and population/households outside the buffer.
- [x] Add time benchmark to key sections of code with `%%time` as the first line of the code block to assess the main contribution of the paper: computational speed on cyberinfrastructure. **Done**.
- [x] How important or efficient is the network simplification function? Does this impact the locations/connectivity of any hospitals? **Done** by counting edges before and after, and by buffering the road network and excluding hospitals beyond the road network.
- [x] Clarify use of packages and functions throughout the code. **Improved** to a great extent, but it would be far easier for novices to understand the methods without all of the extra code for parallel processing or for dynamically choosing the population and the health resource type.
- [x] How are weights justified for the enhanced distance bands? Would different weights significantly change outcomes? **Done** by some previous student reanalyses.
- [x] For reproducibility, we should filter hospital types in the code, rather than beforehand. **Done**, but we could not find original data on ventilators.
- [x] Pay attention to CRSs: are they always transformed when they need to be? Can the final maps be projected? **Done** 
- [ ] Could area-weighted reaggregation be used for the overlap analysis?
- [ ] Why are hexagons used for the analysis as opposed to other spatial data structures, e.g. a raster-like tessellation of squares? In other words, is there a modifiable areal unit problem? Does the use of different sizes and shapes for the unit of analysis matter?
- [ ] Should the default network speed be set to 35mph?

### Spring 2021 class ideas beyond the scope of a reanalysis

- [ ] There are other models besides two-step catchment analysis for spatial interaction in health geography, e.g. gravity model.
- [ ] Could other forms of transit be included? Why is the analysis dependent upon personal vehicle use?
- [ ] Is there a better indicator for hospital capacity other than ventilators or ICU Beds?

### Fall 2023 class questions and ideas for reanalysis

- [ ] 
- [ ] 
- [ ] 
