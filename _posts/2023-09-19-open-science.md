---
layout: lesson
title: Reproducible and Open GIScience
purpose: "debate the roles of open source GIS and Open GIScience"
format: lecture
date: 2023-09-19 11:15
term: fa23
---

## Reading

- NASEM. 2019. *Reproducibility and Replicability in Science*. Washington, D.C.: National Academies Press. [DOI: 10.17226/25303](https://doi.org/10.17226/25303)
  - Chapter 3, *Understanding reproducibility and replicability* (pages 31-43 )
- Rey, S. J. 2009. Show me the code: Spatial analysis and open source. *Journal of Geographical Systems* 11 (2):191–207. [DOI: 10.1007/s10109-009-0086-8](http://dx.doi.org/10.1007/s10109-009-0086-8)
- Dr. Rachel Ainsworth discusses open science culture: <https://youtu.be/c-bemNZ-IqA>

## Discussion

In preparation for this debate, please prepare a reflection/position statement on the two questions in the form of a blog-style post on your GitHub site.
Specifically, you might reflect on:
1. To what extent does **open source GIS** help solve the problems of the **reproducibility crisis for geography**? How?
2. Are there problems with reproducibility and replicability in geography that open source GIS cannot help solve?

While you read these, consider:
- What are the meanings of *free software*, *open source*, and *open science*?
- How is *free* as in the free software movement different from *free* as in a cost of `$0.00`?
- In what way might something be *open source* but not *free*?
- As we practice Open GIScience in this class, what are the implications for:
  - Learning
  - The [Honor Code](/2023/09/12/honorcode)
  - Evaluation & Grades
- Is there space for Open GIScience in an undergraduate liberal arts education?
- What risks/benefits do you see for use of open source GIS in:
  - science?
  - government?
  - private businesses?

We can debate this in the context of this ESRI tool for [managing COVID testing sites](https://www.esri.com/en-us/covid-19/response)

## Resources

- High-profile coronavirus retractions raise concerns about data oversight, [Nature](https://www.nature.com/articles/d41586-020-01695-w)
- NSF Project to create a [geospatial virtual data enclave](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1832465&HistoricalAwards=false) and Doug Richardson's [short article about it](https://www.esri.com/about/newsroom/arcnews/dealing-with-geoprivacy-and-confidential-geospatial-data/) as an alternative to data centers like [Rocky Mountain Research Data Center](https://www.census.gov/about/adrm/fsrdc/locations/rocky-mountain.html)
- Sergio Rey has been central in developing the Python spatial analysis library [PySAL](https://pysal.org/)

### Additional resources on Open GIScience

- Singleton, A. D., S. Spielman, and C. Brunsdon. 2016. Establishing a framework for Open Geographic Information Science. *International Journal of Geographical Information Science* 30 (8):1507–1521. http://dx.doi.org/10.1080/13658816.2015.1137579
- Sui, D., and P. Kedron. 2021. Reproducibility and Replicability in the Context of the Contested Identities of Geography. *Annals of the American Association of Geographers* 111 (5):1275–1283. DOI:[10.1080/24694452.2020.1806024](https://doi.org/10.1080/24694452.2020.1806024).
- Stodden, V. 2014. What computational scientists need to know about intellectual property law: A primer. In *Implementing Reproducible Research*, eds. V. Stodden, F. Leisch, and R. D. Peng, 325–340. Boca Raton: CRC Press.
- The Open Source Geospatial Foundation (OSGeo) take on [open source](https://www.osgeo.org/about/what-is-open-source/)
- The [MIT License](https://opensource.org/licenses/MIT)
- [Creative Commons Licensing](https://creativecommons.org/licenses/)
- GNU's Philosophy of [Free Software](https://www.gnu.org/philosophy/free-sw.en.html) and how [open source misses the point](https://www.gnu.org/philosophy/open-source-misses-the-point.html)
- How is OpenStreetMap [having a moment](https://joemorrison.medium.com/openstreetmap-is-having-a-moment-dcc7eef1bb01) concurrently with the [death of an open source business model](https://joemorrison.medium.com/death-of-an-open-source-business-model-62bc227a7e9b)?

## Landscape of open standards and software

- The Open Geospatial Consortium [(OGC)](https://www.ogc.org/) develops standards, including [simple features standards](https://www.ogc.org/standards/sfa)
- The Open Source Geospatial Foundation [(OSGEO)](https://www.osgeo.org/) supports open source geospatial software and education
- Geometry Engine Open Source (GEOS) is an [open source code library](https://trac.osgeo.org/geos) in C++ for implementing the OGC simple feature standards
- [PROJ](https://proj.org) similarly implements open standards for map projection.
- Who uses GEOS and PROJ?
  - [PostGIS](https://postgis.net/) does!
  - [Shapely](https://pypi.org/project/Shapely/) does, which is in turn used by [GeoPandas](https://geopandas.org/) for spatial data science in Python.
  - [GDAL](https://gdal.org/) too! and everyone uses GDAL, including...
  - [Simple Features for R](https://r-spatial.github.io/sf/), the basis for spatial analysis in R, uses GEOS, PROJ and GDAL.
  - as does [QGIS](https://qgis.org/)!

## A 'Show Me the Code' Example: Distance Matrix in QGIS

The `Distance Matrix` [algorithm documentation](https://docs.qgis.org/3.16/en/docs/user_manual/processing_algs/qgis/vectoranalysis.html#distance-matrix) says nothing about how it calculates distances!

Watch a [video](https://midd.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=855206e6-2da2-4879-b86a-acdf016865e4) of the issue, and/or follow the notes below.

### Reading code to understand an algorithm

- Go to the QGIS GitHub repository [github.com/qgis](https://github.com/qgis) and search for `distancematrix` within the repository
- distance matrix algorithm [source code](https://github.com/qgis/QGIS/blob/f32725658f205af4ac9718d3a3b74f13eaa98d3e/python/plugins/processing/algs/qgis/PointDistance.py)
  - line 179: Transforms the target features into the source CRS (coordinate reference system)
  - line 182: CRS set to source CRS
  - line 183: Ellipsoid set to context ellipsoid
- distance area class [source code](https://github.com/qgis/QGIS/blob/5caa3880ff5e85df9116d191863809c6851644c8/src/core/qgsdistancearea.cpp)
  - line 413: converts to meters
  - the only information passed to `qgisdistancearea` is the context ellipsoid and transformation, and the source crs
- The API (application programming interface) guide can also be a quick and helpful reference to QGIS variables [qgis.org/api](https://qgis.org/api/classQgsProcessingContext.html)
  - there is a `context.ellipsoid()` and a `context.distanceUnit()`, but the distance matrix algorithm never uses `distanceUnit`.

### Conclusions

- `Distance Matrix` appears to calculate distance in `meters`, no matter what.
- Target features are automatically re-projected to match the CRS of input features
- If the input layer uses a projected coordinate system, that system is used or planar distance calculation.
- If the input layer uses a geographic coordinate system, the project ellipsoid is used for ellipsoidal distance calculation.
