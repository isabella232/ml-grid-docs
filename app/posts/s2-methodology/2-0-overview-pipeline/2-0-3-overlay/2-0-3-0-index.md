---
title: ML-derived overlay
date: 2012-08-23
layout: post.html
---

With the probability of a tower computed for each tile, the next step was to compile these results into a GeoJSON and provide this as a map overlay that the mappers could use on top of their satellite imagery. To accomplish this, we needed to select a hard threshold for the probability score. Any image with a score at or above this limit would be designated as having a HV tower by the model and incorporated into the results that would eventually be given to our Data Team during mapping. To choose this threshold, we computed the Receiver Operator Characteristic (ROC) curve, and plotted the distributions of scores for positive and negative examples (i.e., containing or not containing HV towers). These tiles were included in a GeoJSON map that simply marked a square outlining every positive prediction. Here, the threshold was set at 0.97 in an attempt to balance true and false positives. As in the previous inference step, these GeoJSON overlays were computed in batches according to the X-indices of tiles. Finally, all overlays were concatenated into one file using [`geojson-merge`](https://github.com/mapbox/geojson-merge) and uploaded to S3 for the mapping team to download and use within [JOSM](https://josm.openstreetmap.de/) (Java OpenStreetMap; an OSM editor).
