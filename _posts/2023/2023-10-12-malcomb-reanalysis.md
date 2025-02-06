---
layout: lesson
title: Malcomb et al Reanalysis
purpose: "reanalyze the vulnerability model for Malawi and test robustness"
format: lab
term: fa23
date: 2023-10-12 13:30
---

The purpose of this lab is to:

- choose a parameter or set of interdependent parameters of the Malcomb et al climate vulnerability model for Malawi which represents a subjective researcher decision
- change the parameter or set of parameters
- test the vulnerability model's robustness to the change
- visualize and interpret your results in the context of theory on error and uncertainty in spatial models in general and vulnerability models in particular

## Procedure

- **identify** an error, uncertain decision, or opportunity for improving reproducibility or study design. Everyone can contribute to the following on this reproduction:
  1. Finalize one cohesive report. I will do as much of this as I can before lab...
  2. Investigate metadata documentation for the data sources and integrate what you learn into the report. Metadata is found in the `data/metadata` folder. and the `data_metadata.csv` file tells you which metadata files are associated with which data inputs. This investigation may lead to aspects of the study that you want to change.
- **write** a plan for modifications in markdown, including:
  1. title and author (yourself)
  2. description of modification(s) with rationale(s)
  3. plan for visualizing/comparing/interpreting of results
  4. save as `docs/reports/<name>-analysis-plan.md`, e.g. `docs/reports/holler-analysis-plan.md`
  5. `commit` the plan and `push` to GitHub
  6. this is a small-scale version of a [preregistration](https://www.cos.io/initiatives/prereg)
- **modify** the main `01-Rpr-Malcomb-2014.Rmd` analysis plan & code to address the issue identified above
- **implement** the change in code
- **interpret** the results of your change(s) in the `rmarkdown` report
- **knit** a new study report `html` form. See [this video](https://midd.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=9cc5514a-2c8a-42b9-a974-b08b01190226)
- enable **GitHub Pages** on the repository to serve the `html` version of the report to the web. (see previous video)
- **write** a blog post highlighting what you have `learned from` and `contributed to` with this reproduction and reanalysis study. In particular, the report and blog should address error and uncertainty in the Malcomb et al study in the context of Longley's and Tate's frameworks.
  - Keep in mind, a blog post is for **highlights** : aim for a post to be a short and impactful advertisement for the full study... no more than two paragraphs.
- **Link** to your full study from the blog post   

## Timeline

- Thursday, October 12 Lab: Finalize analysis plan and commit the plan to GitHub
- Before Thursday, October 19 Lab: Commit finalized analysis report and blog post to GitHub
