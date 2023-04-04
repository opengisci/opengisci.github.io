---
layout: default
title: Open GIScience
---

# Fall 2023 Open GIScience

*note*: Most of the content here has yet to be updated from Fall 2021.

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
