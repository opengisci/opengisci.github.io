---
layout: default
title: Open GIScience
---

Looking for Data Science Across the Disciplines?  
It's here: [opengisci.github.io/dsad/](https://opengisci.github.io/dsad/)

# Fall 2023 Open GIScience

In this course, we will study geographic information science (GIScience) by reproducing published research with open-source geospatial software.
We will debate issues in GIScience by applying critical GIS scholarship, fundamentals of spatial data and analysis, and evidence from our reproduction studies.
We will practice open GIScience by collaboratively developing research plans, acquiring and describing spatial data, analyzing and visualizing data with SQL and R, and testing for error and uncertainty.
Our research products and results will be published with open science standards in public portfolios.
We typically investigate research with themes of human-environment interactions, health, hazards, urban development, and more.
These research themes require and integrate social/demographic data, environmental data, and big data.

## Fall 2023

Meeting | Lesson
:-----: | :----:
{% for post in site.posts reversed -%}
{%- if post.term == "fa23" -%} {%- if post.format -%} {{ post.date | date: '%b-%d' }} {{ post.format | capitalize }} {% endif %} | <a href="{{ post.url }}" {% if post.format == "break" %} style="color: black" {% endif %}>{{ post.title }}</a>
{% endif -%}
{% endfor %}

## Members of Fall 2023

[alanalutz](https://alanalutz.github.io)  ~
[alexxuyide](https://alexxuyide.github.io)  ~
[andreyjcao](https://andreyjcao.github.io)  ~
[andya17](https://andya17.github.io/)  ~
[audreyrpark](https://audreyrpark.github.io)  ~
[azalecki](https://azalecki.github.io)  ~
[benjamincordola](https://benjamincordola.github.io)  ~
[colman-bashore](https://colman-bashore.github.io)  ~
[eliseylchan](https://eliseylchan.github.io)  ~
[gshanleybarr](https://gshanleybarr.github.io)  ~
[gsokolow](https://gsokolow.github.io)  ~
[isaiahbennett2](https://isaiahbennett2.github.io)  ~
[katieheo](https://katieheo.github.io)  ~
[sydalexander](https://sydalexander.github.io)  ~
[t-sutter](https://t-sutter.github.io)  ~
[whprocter](https://whprocter.github.io)

## Resources and previous courses

- *Human-Environment and Geographical Sciences (HEGS) Reproducibility and Replicability*  research and broader impacts activities are available at [HEGSRR.github.io](https://HEGSRR.github.io), [www.github.com/HEGSRR](https://www.github.com/HEGSRR) and [osf.io/c5a2r/](https://osf.io/c5a2r/)
- Previous versions of the Open Source GIScience course (Fall 2019, Spring 2021, and Fall 2021) are available at [gis4dev.github.io](https://gis4dev.github.io)
- Open Source GIS for Development course content (Spring 2014, Spring 2015, and Spring 2018) can be found in the [GIS4DEV course manual](https://gis4dev.github.io/assets/GIS4DEV.pdf)
