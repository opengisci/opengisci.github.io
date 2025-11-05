---
layout: default
title: Open GIScience
---

# Open GIScience

In this course, we will study geographic information science (GIScience) by reproducing published research with open-source geospatial software.
We will debate issues in GIScience by applying critical GIS scholarship, fundamentals of spatial data and analysis, and evidence from our reproduction studies.
We will practice open GIScience by collaboratively developing research plans, acquiring and describing spatial data, analyzing and visualizing data with SQL and R, and testing for error and uncertainty.
Our research products and results will be published with open science standards in public portfolios.
We typically investigate research with themes of human-environment interactions, health, hazards, urban development, and more.
These research themes require and integrate social/demographic data, environmental data, and big data.

## Spring 2025

Meeting | Lesson
:-----: | :----:
{% for post in site.categories.sp25 reversed -%}
{%- if post.format -%} {{ post.date | date: '%b-%d' }} {{ post.format | capitalize }} {% endif %} | <a href="{{ post.url }}" {% if post.format == "break" %} style="color: black" {% endif %}>{{ post.title }}</a>
{% endfor %}

## Members of Spring 2025

- [gushoward](https://gushoward.github.io)
- [DermotMcMillan](https://DermotMcMillan.github.io)
- [jorredahl](https://jorredahl.github.io)
- [lnerbonne](https://lnerbonne.github.io)
- [mkahngmills](https://mkahngmills.github.io)
- [padutchfan123](https://padutchfan123.github.io)

## Resources and previous courses

- [Simple Features in R](https://opengisci.github.io/Learn-Simple-Features/)
- Winter 2025 Data Science Across the Disciplines [Geography Section](https://opengisci.github.io/dsad/) and [Notebook](https://opengisci.github.io/dsad25_book/)
- Fall 2023 [Open GIScience]({% link fa23.md %})
- *Human-Environment and Geographical Sciences (HEGS) Reproducibility and Replicability*  research and broader impacts activities are available at [HEGSRR.github.io](https://HEGSRR.github.io), [www.github.com/HEGSRR](https://www.github.com/HEGSRR) and [osf.io/c5a2r/](https://osf.io/c5a2r/)
- Previous versions of the Open Source GIScience course (Fall 2019, Spring 2021, and Fall 2021) are available at [gis4dev.github.io](https://gis4dev.github.io)
- Open Source GIS for Development course content (Spring 2014, Spring 2015, and Spring 2018) can be found in the [GIS4DEV course manual](https://gis4dev.github.io/assets/GIS4DEV.pdf)
