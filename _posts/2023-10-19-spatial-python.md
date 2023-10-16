---
layout: lesson
title: Introductory Spatial Python
purpose: "practice using Python Jupyter notebooks and GeoPandas with cyberinfrastructure"
format: lab
date: 2023-10-19 13:30
term: fa23
---



## Technology Context

- [Python](https://www.python.org/) is the most popular programming langauge for (spatial) data science. 
- [Anaconda](https://www.anaconda.com/) is a system for managing computational environments using Python and python software packages.
- [JupyterLab](https://jupyter.org/) is the next generation of JupyterNotebooks, a prime example of a [computational notebook](https://www.nature.com/articles/d41586-018-07196-1). Notebooks can run Python code.
- [Pandas](https://pandas.pydata.org/) provides SQL-like database structures and functions
- [GeoPandas](https://geopandas.org/) provides spatial analysis functions
- Much of GeoPandas is based on [Shapely](https://shapely.readthedocs.io) geometry types and functions
- [PySAL](https://pysal.org/) implements advanced spatial analysis and statistics, building off of the GeoPandas package
- [Quarto](https://quarto.org/) is the python / Jupyter solution for rendering pretty manuscripts, books, and websites from Jupyter notebooks

## Spatial data science with python on your own

What if you want to use Python and Jupyter notebooks to practice spatial data science on your local computer, without access to servers like Hour of CI and CyberGISX? You can install [Anaconda](https://www.anaconda.com/) and create a local conda environment including Jupyter notebooks and packages for spatial data science. The `pandas` package provides the database functions you learned to love in `SQL` while the `geopandas` package provides the spatial functions, analogous to `PostGIS`.

## Cheat Sheets

- [Pandas](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
- [DataCamp Cheat Sheets](https://www.datacamp.com/community/data-science-cheatsheets)

## Resources

- [How to set up Anaconda and Jupyter Notebook the right way](https://towardsdatascience.com/how-to-set-up-anaconda-and-jupyter-notebook-the-right-way-de3b7623ea4a)

### Introductory Spatial Python CyberGISX Tutorials in Transition

I-GUIDE will eventually house a solid collection of introductory tutorials and workshops, but the infrastructure is currently in transition.

- From [CyberGISX Hub](https://cybergisxhub.cigi.illinois.edu/), you can log in to CyberGISX and browse [COVID-19](https://cybergisxhub.cigi.illinois.edu/wherecovid-19) and [Community](https://cybergisxhub.cigi.illinois.edu/notebooks) Notebooks
- We can gain a solid introduction to spatial analysis in Python with Jupyter notebooks through a series of tutorial notebooks developed by Rebecca Vandewalle.
- Each notebook has an Open with CyberGISX button, which will copy the notebook contents from its GitHub repository into your personal CyberGISX account and launch the notebook.
- Let's try three introductory notebooks, in this sequence:
- [Jupyter Notebooks Quick Start](https://cybergisxhub.cigi.illinois.edu/notebook/jupyter-notebooks-quick-start-2/)
- [Introduction to Python Programming](https://cybergisxhub.cigi.illinois.edu/notebook/introduction-to-python-programming/)
- [Python Geospatial Libraries](https://cybergisxhub.cigi.illinois.edu/notebook/python-geospatial-libraries/) *note:* this tutorial is found in `cybergis-jupyter-notebook-repo/python_intro/Python_Geospatial_Libraries_p3.py`
- Python files for the code
  - [Python Intro](/assets/python-intro.py)
  - [Geospatial Python](/assets/python-geospatial.py)
