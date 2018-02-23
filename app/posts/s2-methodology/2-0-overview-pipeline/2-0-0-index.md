---
title: The processing pipeline
date: 2012-09-28
layout: post.html
---

Generating country-wide maps involved several key steps outlined below and discussed in detail:

1. Obtain country boundaries for Pakistan, Zambia, and Nigeria 
2. Compute all satellite imagery tile indices within those bounds
3. Train a machine learning model to compute the probability that a HV towers was present in a single image using a small training set from each country
4. Using trained model, compute these probabilities across all three countries
5. Compile the highest probability results into a GeoJSON overlay that indicated the most likely HV tower locations. 
6. Manually map HV infrastructure (specifically towers and substations) using the overlay
