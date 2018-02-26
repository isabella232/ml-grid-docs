---
title: The processing pipeline
date: 2012-09-28
layout: post.html
---

Generating country-wide maps involved several key steps outlined below and discussed in detail:

1. Download imagery for Pakistan, Zambia, and Nigeria after obtaining country boundaries and computing tile indices
1. Train and apply a machine learning model to compute the probability that a HV tower was present in a single image using a small training set from each country. Then apply the model at a country-wide scale
1. Compile the highest probability results into a GeoJSON map overlay that indicated the most likely HV tower locations.
1. Trace HV infrastructure (specifically towers, lines, and substations) using the ML-derived overlay to focus on high-value areas.
