---
layout: lesson
title: "Disability and COVID-19 Reproduction"
purpose: "reanalyze county-level association of disability and COVID-19"
format: lab
date: 2023-09-28 13:30
term: fa23
---

The purpose of this lab is to reanalyze Chakraborty (2021) and finalize a reproduction report.

## Procedure

- **identify** an error, uncertain decision, or opportunity for improving reproducibility or study design. There are at least two things everyone should work on for this reproduction:
  1. The final choropleth map has a mistaken parameter causing it to only use half of the available color ramp.
  2. move the "rational for the updated report" section to the very end
  3. Improve the formatting of the missing data table with `Kable` and/or `KableExtra` functions and/or by transposing the table to vertical orientation.
  3. Integrate Emily's discussion and any new results that have yet to be discussed into a new discussion section. There's no need to repeat information found earlier in the report. Rather, this is a chance to synthesize the findings presented earlier and think about their implications.
  4. Separate a conclusions section from the discussion that concludes whether the reproduction attempt was successful, and what the implications are for how the original study contributes to scientific knowledge.
- **write** a plan for modifications in markdown, including:
  1. title and author (yourself)
  2. description of modification(s) with rationale(s)
  3. plan for visualizing/comparing/interpreting of results
  4. save as `docs/reports/<name>-analysis-plan.md`, e.g. `docs/reports/holler-analysis-plan.md`
  5. `commit` the plan and `push` to GitHub
  6. this is a small-scale version of a [preregistration](https://www.cos.io/initiatives/prereg)
- **modify** the main `01-Rpr-Chakraborty.Rmd` analysis plan & code to address the issue identified above
- **implement** the change in code
- **interpret** the results of your change(s) in the `rmarkdown` report
- **knit** a new study report in `pdf` and `html` forms. See [this video](https://midd.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=9cc5514a-2c8a-42b9-a974-b08b01190226)
- enable **GitHub Pages** on the repository to serve the `html` version of the report to the web. 
- **write** a blog post highlighting what you have `learned from` and `contributed to` with this reproduction and reanalysis study. In particular, please address these questions:
  - What have you learned from doing a reproduction study?
  - Has the reproduction deviated from the original study in any way?
  - If so, are the deviations improvements or errors?
  - Are there opportunities to further improve the study's research design, reproducibility, or reproducibility for teaching purposes?
  - Are there opportunities to design meaningful replication studies to further test any theories established by this study?
- Keep in mind, a blog post is for **highlights** : aim for a post to be a short and impactful advertisement for the full study... no more than two paragraphs.

## Timeline

- Thursday, September 28 Class: Draft analysis plan of proposed changes and plans for interpreting the changes
- Thursday, September 28 Lab: Finalize analysis plan and commit the plan to GitHub
- Before Thursday, October 5 Lab: Commit finalized analysis report and blog post to GitHub

## Suggested markdown for analysis plan

```markdown
# Planned revisions to reproduction of ....

Author: First name, Last name

## Analysis

Enumerate and justify changes to analytical plan here

## Results

Describe how changes will be visualized / compared here

## Discussion

Describe how you will interpret the results of your changes here.
For example, in hypothetical terms, if my new/revised map shows ---, it will mean that ---.
```
