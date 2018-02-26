---
title: Tracing
date: 2012-08-23
layout: post.html
---

Using the GeoJSON overlay, the data-team began to trace all HV infrastructure. They first created a “task” for each country using a tasking manager. This tool breaks a geospatial area into a grid of small squares, where any person can only work on mapping a single small region at a time (to prevent collisions; Figure XXX). 


<figure class="align-center">
  <img src="/assets/graphics/content/tasking_manager_example.png" alt="Tasking manager" />
  <figcaption><b>Figure XXX. Example of tasking manager in Zambia.</b> Each yellow square represents a small region that was mapped and each blue square shows a locked region where mapping in progress by a single person. Squares without any color still require attention.</figcaption>
</figure>

Each person selects and “locks” a square before mapping all HV features that lie within this small zone using JSOM. Each square was approximately 1,100 km2, which often contained many predicted towers distributed throughout the area. ![screen shot 2018-02-22 at 2 07 18 pm](https://user-images.githubusercontent.com/1152236/36558723-ed712e92-17d9-11e8-86de-70506d74339e.png)


Most of this work was comprised of tracing from tower to tower. Again, the ML-derived overlay acted as a guide -- HV towers that were correctly identified showed up as strings of small boxes that are visible against the unordered background of false positives. Each day, the Data Team updated the HV infrastructure within their mapping software to make sure they always edited the most up-to-date version. Because it was difficult to keep track of which areas had been reviewed, the Data Team customized the To-Fix plugin available in JOSM. Rather than manually zoom and pan between each predicted tower, this allowed them to load in the ML-derived prediction map and iterate over individual predictions one at a time with the click of a button. This helped organize the review process and increased the speed of each mapper. The Data Team traced every tower and power substation they could find (even if it was not identified in the ML portion of the pipeline). In this way, the GeoJSON overlay acted as a guide so that the mappers could efficiently hook into a section of the network and begin mapping, but it did not dictate all of their mapping efforts.

Once each tasked region in the tasking manager was mapped, the team then went back and validated each region. Here, the goal is to double check for any missing connections and verify the accuracy of all added features (e.g., HV towers and substations). As edits were made within OSM itself, all additions are available to view in OSM. We then computed final stats on the mapping rate (in of km2 per hour and towers per hour) during the generation of training data and during country-wide prediction (i.e., before and after the ML overlay was available). These two data points allowed us to calculate the relative speed of pure manual mapping and ML-assisted mapping.
