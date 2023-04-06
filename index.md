---
layout: default
title: Open GIScience
---

# Fall 2023 Open GIScience

In this course, we will study geographic information science (GIScience) by reproducing published research with open-source geospatial software.
We will debate issues in GIScience by applying critical GIS scholarship, fundamentals of spatial data and analysis, and evidence from our reproduction studies. We will practice open GIScience by collaboratively developing research plans, acquiring and describing spatial data, analyzing and visualizing data with SQL and R, and testing for error and uncertainty. Our research products and results will be published with open science standards in public portfolios. We typically investigate research with themes of human-environment interactions, health, hazards, urban development, and more. These research themes require and integrate social/demographic data, environmental data, and big data.

*note*: Most of the content here has yet to be updated from Fall 2021.

## 2023

Meeting | Lesson
------- | ------
{% if post.term == "fa23" %}
{% for post in site.posts reversed -%}
{%- if post.format -%} {{ post.date | date: '%b-%d' }} {{ post.format | capitalize }} {% endif %} | <a href="{{ post.url }}" {% if post.format == "break" %} style="color: black" {% endif %}>{{ post.title }}</a>
{% endif %}
{% endfor %}

## All

Meeting | Lesson
------- | ------
{% for post in site.posts reversed -%}
{%- if post.format -%} {{ post.date | date: '%b-%d' }} {{ post.format | capitalize }} {% endif %} | <a href="{{ post.url }}" {% if post.format == "break" %} style="color: black" {% endif %}>{{ post.title }}</a>
{% endfor %}

## Members of Fall 2023

*t.b.d*

## Resources and previous courses

- Reproducibility and Replicability in Human-Environment and Geographical Sciences (HEGS) available at [HEGSRR.github.io](https://HEGSRR.github.io) and [osf.io/c5a2r/](https://osf.io/c5a2r/)
- Previous versions of the Open Source GIScience course (Fall 2019, Spring 2021, and Fall 2021) are available at [gis4dev.github.io](https://gis4dev.github.io)
- Open Source GIS for Development course content (Spring 2014, Spring 2015, and Spring 2018) can be found in the [GIS4DEV course manual](https://gis4dev.github.io/assets/GIS4DEV.pdf)
- University Consortium for GIS (UCGIS) [2020 Symposium](https://www.ucgis.org/symposium-2020) [Presentation Slides](/assets/teachingReproducibility.pdf)
- Using GitHub for [teaching & research](github-academics)
