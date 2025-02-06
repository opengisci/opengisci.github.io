---
layout: lesson
title: COVID-19 Spatial Accessibility Reproduction
purpose: "reproduce COVID-19 spatial accessibility"
format: lab
date: 2023-11-02 13:30
term: fa23
---

The goal of this lab is to get accustomed to working in a cyberinfrastructure environment with Python, Jupyter notebooks, and GitHub integration, and understand how to implement spatial accessibility analysis in Python.
We will do so with the Jupyter notebook published to accompany [Kang et al (2020)](https://doi.org/10.1186/s12942-020-00229-x).
The notebook has been published on [CyberGISX](https://cybergisxhub.cigi.illinois.edu/notebook/rapidly-measuring-spatial-accessibility-of-covid-19-healthcare-resources-a-case-study-of-illinois-usa/) and maintained in a [GitHub repository](https://github.com/cybergis/COVID-19AccessibilityNotebook).
We have published the results of our prior reproduction and reanalysis studies in this repository: <https://github.com/HEGSRR/RPr-Kang-2020>

By the end of lab, you should have:
- executed the complete notebook
- taken notes and added comments to the code cells and/or content to the markdown cells in the notebook on CyberGISX to understand how the code relates to the publication (i.e. which blocks of code implement which sections of the paper?)
- pushed your changed (annotated) version of the notebook back to your own GitHub repository

## Instructions

- Let's continue working in groups as we did for the Spielman et al replication.

### Set up GitHub for Integration with CyberGISX

- Fork the [Rpr-Kang-2020](https://github.com/HEGSRR/RPr-Kang-2020) repository 
- Set up an authentication token for connecting GitHub and CyberGISX
    - Go to your GitHub User account settings
    - at the Bottom of the settings menus, find `Developer Settings`
    - go to Personal access tokens --> `Generate new token` --> `Generate new token (classic)` 
    - You can give the token the name `cybergisx`
    - In terms of `scopes` for this token, you only need the first scope: `repo`
    - You will need this authentication token for communicating between CyberGISX and GitHub.
- Here is the GitHub documentation on [personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

### Set up CyberGISX

- Log into Google services (e.g. drive.google.com) using your Middlebury credentials
- Go to the CyberGISX Hub <https://cybergisxhub.cigi.illinois.edu/>
- At the top-right, of the page, `Register with CILogon` and create and account / log in using `Google` and your `@middlebury.edu` Google account as your Identity Provider
- Fill out the registration form with `organization`: Middlebury College, `website link`: your google site and `class`: Open GIScience
- Once you are logged in, `Launch CyberGISX` at the top-right

### Linking CyberGISX and GitHub

- Go to `Git` and `Add a remote repository` to clone your `Rpr-Kang-2020` repository into the CyberGISX servers using the web address of your repository on GitHub
- Try making a small change.
  - E.g. open the main `readme.md`, add your name to the list of authors, and save `readme.md` as a markdown file
- Open the `Git` panel from the Git icon at the left
- The Git menu shows `changed` files 
- Click the plus button on changed files to `stage` the change, moving the file to `staged`
- Write a `summary` of changes at the bottom of the Git panel
- `Commit` the changes with your GitHub name and email address.
- At the top of the panel, an upload cloud icon will have an orange dot to `push` the changes to GitHub.
- To `push`, you will need your GitHub user name and authentication token.
- Check to see if the change(s) is/are reflected on GitHub.com
- Always remember to pull new changes into a work session as you begin and push important changes from a work session as you conclude!

### Executing a notebook

- One advantage of using a JupyterHub server is that server administrators can set up multiple Python environments from which to choose. For this lab, let's use the default `Python 3` environment.
- Switch to the file browser panel and find the `procedure\code\02_COVID-19_Acc-Original.ipynb` notebook
- Verify that the `kernel` processing environment for the notebook is `Python 3` (at top-right corner of the notebook)
- Because this environment is already set up, you *do not need to install* any packages!
- Run the notebook. There are three decisions to make in order to create different outputs, so I suggest group members try different combinations of these decisions:
  - Street network: buffered or not?
  - Population: people over 50, or COVID patients?
  - Service: ICU beds, or ventilators?
- Note how long the hospital catchment process took to run and enter results in this [GOOGLE FORM](https://forms.gle/i1Hk3qZdFMhwk2nj7)
- Save results, and then open `procedure\code\03_COIVD-19_Acc-Reanalysis.ipynb`
- Execute the code, trying differnet combinations of Population and Service
- Note how long the hospital catchment process took to run and enter results in this [GOOGLE FORM](https://forms.gle/i1Hk3qZdFMhwk2nj7) 
- Take notes on how this reanalysis different from the original notebook.

Transitioning to next week you should:
- Compare the code repository to the published paper and brainstorm ways in which the code repository could be improved with regards to computational efficiency/speed, reproducibility, uncertainty, errors, cartography, aesthetics, readability...

 ## Software References

- Python package for OpenStreetMap and specifically for network data in OSM: osmnx [documents](https://osmnx.readthedocs.io/en/stable/), [repository](https://github.com/gboeing/osmnx) and [examples repository](https://github.com/gboeing/osmnx-examples), and repository for version [0.11.4](https://github.com/gboeing/osmnx/releases/tag/v0.11.4)
- Python package for network analysis: [networkx](https://networkx.org/)

## Reference

Kang, J. Y., A. Michels, F. Lyu, Shaohua Wang, N. Agbodo, V. L. Freeman, and Shaowen Wang. 2020. Rapidly measuring spatial accessibility of COVID-19 healthcare resources: a case study of Illinois, USA. *International Journal of Health Geographics* 19 (1):1–17. DOI:[10.1186/s12942-020-00229-x](https://doi.org/10.1186/s12942-020-00229-x).
