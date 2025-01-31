---
title: The processing pipeline
date: 2018-02-27
layout: post.html
---

Generating country-wide maps involved several key steps outlined below and discussed in detail:

1. Download imagery for Pakistan, Zambia, and Nigeria after obtaining country boundaries and computing tile indices.
1. Train a machine learning model to compute the probability that a HV tower was present. Then, apply the model at a country-wide scale.
1. Compile the highest probability results into a GeoJSON map overlay that indicated the most likely HV tower locations.
1. Trace HV infrastructure (specifically towers, lines, and substations) using the ML-derived overlay to focus on high-value areas.
