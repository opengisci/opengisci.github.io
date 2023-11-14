---
layout: lesson
title: "Independent Project Ideas"
purpose: "generate feasible ideas for an independent project"
format: lecture
term: fa23
---

During this lesson, we will discuss and decide upon project ideas.
Projects should be similar in difficulty and scope to one of the four labs this semester, and should encompass a research study using spatial analysis with open source GIS technology.
Projects should contribute to at least one of these goals:
- increasing transparency/reproducibility
- increasing our knowledge about a theory / process through replication
- 

## Fall 2023 Project Ideas

- Complete Spielman et al replication by analyzing the index stability over time (pre-analysis plan has been written)
- Complete Chakraborty replication with new data (pre-analysis plan and preliminary work has been done)
- Replicate social media studies of disaster as in <https://github.com/GIS4DEV/OR-Dorian>
- Reproduce wildlife corridor analysis in R or Python, which has been done in QGIS model builder with some SAGA tools
- Replicate data analysis of rainfall and/or river flow for Vermont 2023 storms, ideally starting with R scripts from the USGS <https://owi.usgs.gov/R/> (has this site changed? alternative sources may be <https://github.com/orgs/USGS-R/repositories> or <https://www.usgs.gov/mission-areas/water-resources/science/science-topics/data-science> )
- Replicate any of the studies we have done in different geographic regions, for different time periods, or otherwise with different data
- Otherwise significantly modify the methods approach for any of the studies we have done.
- Treat tutorial or lab problems from introductory GIS as studies to reproduce, and create R or Python code to solve the problem. 
- Reproduce any studies on CyberGISX / I-GUIDE / Hydroshare 
- Propose another idea!

### How to identify other project ideas

- Attempt to reproduce a straightforward published research study, especially one published with data and code, or with easily accessible public data sources. Reproduction will likely include some degree of reanalysis, in which some parameters of the study are intentionally changed to improve study design or facilitate learning. If you search for new papers, try adding terms like "R", "Python" or "GitHub" to the search. 
- [CyberGISX](https://cybergisxhub.cigi.illinois.edu/notebooks-discovery/) and [Hydroshare](https://www.hydroshare.org/) all contain published projects. 
- Develop a project to learn a new package or technology for geospatial analysis or visualization.
- Replicate an existing study by substantially changing the geographic and/or temporal context

### Requirements and Expectations

- The independent project will be due with the final GitHub site portfolio, during finals week.
- Projects may be completed in Python, R, or PostGIS SQL. Other languages or open GIS systems may be possible with approval.
- Students may choose to work on very similar projects and troubleshoot challenges with one another, but should maintain thier own complete version of the project and disclose collaboration through authorship and a paragraph in their report referencing [CRediT roles](https://credit.niso.org/)
- Projects should include a **reproducible research compendium** in the form of a GitHub repository, paired with a report/blog post on your main GitHub site.
- You may ask the professor for feedback on the project up to `Monday, December 11`.

#### Procedure

- Start a new repository with the <https://github.com/HEGSRR/HEGSRR-Template> `Use this template` feature
- Customize the `readme.md` with project information
- Populate either the python notebook or Rmarkdown file with an *analysis plan*
- If your chosen study already has data available, populate the data folders with the available data
- Use the `metadata_template.md` template to create a metadata document for each data layer input and saved output
- Update the index tables `data_index.csv` and `procedure_index.csv` 
- Commit and push the repository before you start running anlaysis
- Implement analysis in your Jupyter python notebook or Rmarkdown file
- Add results, discussion, and conclusion sections
- Render/save an `.html` version of the final study
- Link to the rendered report from the main `readme.md`
- Final round of checking and revising metadata documents, `data_index.csv`, `procedure_index.csv` and `results_index.csv`
- *Short* blog post highlighting the study and linking to the 1) repository and 2) html report. Seriously, just a paragraph or two is sufficient to highlight your contributions and link to the study.
