---
author: Sparsh Gupta
categories:
- UTD
- Python
date: "2024-04-30"
draft: false
excerpt: Satellite data is a unique and valuable tool for studying agriculture. Participants considered using optical data from Sentinel-2 and Landsat and radar data from Sentinel-1 in this challenge.
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/gsparsh220598/Rice-Crop-Prediction
subtitle: An Graduate ML project
tags:
- hugo-site
title: is it a rice field?
---
---

## Problem Statement
- The challenge's goal is to predict the presence or non-presence of rice crops at a given location.
- This challenge will consider satellite data from the European Copernicus (Sentinel-1 and Sentinel-2) program and NASA's Landsat program.

## Data Extraction
Satellite data is a unique and valuable tool for studying agriculture. Participants considered using optical data from Sentinel-2 and Landsat and radar data from Sentinel-1 in this challenge. All of these datasets are readily available from the Microsoft Planetary Computer ([HERE](https://planetarycomputer.microsoft.com/catalog)). Participants can choose one or more of these satellite datasets for their solution.
- Extracting data over An Giang province in the Mekong Delta in Vietnam.
- 5x5 bounding boxes from November 2021 to August 2022

### Optical Data from Sentinel-2
Quality Landsat data has been around since the early 1980s with a spatial resolution of 30 meters per pixel and a revisit of 16 days for one mission. We currently have two operational missions (Landsat-8 and Landsat-9) yield 8-day revisits at any location. The launch of the European Copernicus Sentinel-2 missions in 2015 and 2017 added new optical data at a higher 10-meter spatial resolution and a revisit every ten days with one mission and every five days with two missions. So, the combination of Landsat and Sentinel-2 missions (4 total) can observe the ground four times every ten days. This coverage combination can yield coincident revisits about nine times per year, but five days between views of the ground is the best. But, the issue with optical data is that it cannot penetrate clouds. So, the data is not usable if a cloud is over any given location. In the case of Vietnam, clouds are persistent over any one location about 2/3 of the time, so only 1/3 of the data is available in a given year. In addition, our ability to identify these clouds in the data could be better, so we often have issues with data contaminated by clouds, which impacts the results of models.
Optical data (e.g., Landsat or Sentinel-2) contains many spectral bands (e.g., Red, Green, Blue, Red-Edge, NIR, SWIR, etc.) that can be related to the presence or growth of rice crops. As you review the references, you will find that researchers often use statistical combinations of these bands, called indices, to build models. One of the more common indices for agriculture is the Normalized Difference Vegetation Index (NDVI). Still, many others exist, including the Enhanced Vegetation Index (EVI) and the Soil Adjusted Vegetation Index (SAVI). Optical data is used to measure the "greenness" of vegetation during the growth cycle. Differences in band or index values can be used to distinguish differences in crop types (see Figure) and crop yield.