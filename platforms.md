---
title: "Data Platforms"
teaching: 15
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions

- Where does geospatial and demographic data come from?
- Why do these platforms require accounts?
- How do these data sources connect to social science research?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand what each data platform provides and why it matters
- Know which platform to use for a given type of data

::::::::::::::::::::::::::::::::::::::::::::::::

## Overview

Throughout this workshop you will work with satellite imagery, elevation models, census demographics, and shared code. Each of these comes from a different platform, and each platform requires a free account so you can search, download, and use its data. This page explains what each platform offers and why it matters for social science research.

---

## USGS EarthExplorer

👉 [earthexplorer.usgs.gov](https://earthexplorer.usgs.gov)

EarthExplorer is run by the **U.S. Geological Survey** and is one of the largest public archives of remotely sensed data in the world. Through it you can access satellite imagery (Landsat, ASTER), aerial photography, and digital elevation models (DEMs) — all free of charge.

In social science research this data is useful for studying land use change over time, urban sprawl, environmental justice, disaster impacts, and the physical geography of the communities you are analyzing. During the workshop we will use EarthExplorer to download elevation data and satellite scenes that we then visualize and analyze in QGIS.

An account is required to download any data from the archive.

---

## Copernicus Data Space

👉 [dataspace.copernicus.eu](https://dataspace.copernicus.eu)

Copernicus is the **European Union's Earth observation programme**. Its Data Space provides free access to imagery from the Sentinel satellite constellation, which captures the entire Earth's surface every few days at high resolution.

Sentinel-2 imagery is especially valuable for monitoring vegetation health, water bodies, and land cover — all of which intersect with social science questions around agriculture, environmental policy, and community resilience. During the workshop we will use Sentinel-2 data alongside the Esri Sentinel-2 Explorer to visualize land use and land cover change.

An account is required to search and download Sentinel datasets.

---

## U.S. Census Bureau API

👉 [census.gov/data/developers.html](https://www.census.gov/data/developers.html)

The Census Bureau API gives you programmatic access to the **American Community Survey (ACS)**, the **Decennial Census**, and dozens of other demographic datasets — directly from Python code, without manually downloading files.

This is the backbone of quantitative social science research in the United States. With an API key you can pull population counts, income distributions, housing characteristics, and other variables at geographies ranging from the entire nation down to individual census tracts and block groups. During the workshop we will retrieve census data in a Jupyter Notebook, clean it, and produce maps and charts of population trends.

An API key is free and is required for any programmatic data retrieval.

---

## GitHub

👉 [github.com](https://github.com)

GitHub is a platform for **version control and collaboration** built on Git. It hosts code, documentation, and data files in repositories that can be shared, forked, and collaboratively edited.

For this workshop, GitHub serves two purposes. First, the exercise notebooks and workshop materials are hosted in GitHub repositories, and Google Colab pulls directly from them. Second, on Day 2 we will discuss how to share research outputs, manage Carpentries lesson modules, and collaborate on code — all of which rely on GitHub.

An account is required to fork repositories, contribute changes, and access certain materials.

---

::::::::::::::::::::::::::::::::::::: keypoints

- USGS EarthExplorer provides free satellite imagery and elevation data for studying landscapes and environmental change.
- Copernicus Data Space offers high-resolution, frequently updated Sentinel imagery for land cover and vegetation analysis.
- The Census Bureau API enables programmatic access to U.S. demographic data at fine geographic scales.
- GitHub hosts the workshop materials and supports collaborative sharing of code and research outputs.

::::::::::::::::::::::::::::::::::::::::::::::::
