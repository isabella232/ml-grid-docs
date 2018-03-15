---
title: 4. Tracing
date: 2018-02-27
layout: post.html
---

Using the GeoJSON overlay, the data-team began to trace all HV infrastructure. They first created a “task” for each country using a [tasking manager](https://github.com/hotosm/tasking-manager). This tool breaks a geospatial area into a grid of small squares, where any person can only work on mapping a single small region at a time (to prevent collisions; Figure 8).

<figure class="align-center">
  <img src="/assets/graphics/content/tasking_manager_example.png" alt="Tasking manager" />
  <figcaption><b>Figure 8. Example of tasking manager in Zambia.</b> Each yellow square represents a small region that was mapped and each blue square shows a locked region where mapping in progress by a single person. Squares without any color still require attention.</figcaption>
</figure>

Each person selects and “locks” a square before mapping all HV features that lie within this small zone using JSOM. Each square was approximately 1,100 km<sup>2</sup>, which often contained many predicted towers distributed throughout the area (Figure 9). 

<figure class="align-center">
  <img src="/assets/graphics/content/task_manager_tile.png" alt="Tasking manager tile" />
  <figcaption><b>Figure 9. Example of a single locked tile from the task manager.</b> Each dot represents a positive prediction by the model ready to be manually reviewed.</figcaption>
</figure>


Nearly all of the manual tracing involved tracing from tower to tower. Again, the ML-derived overlay acted as a guide -- HV towers that were correctly identified showed up as strings of small boxes that are visible against the unordered background of false positives. The Data Team updated the HV infrastructure within their mapping software each morning to make sure they always edited the most up-to-date version. Tracing primarily involved adding sections of the HV network that were completely missing or adding missing towers along an existing but undermapped HV line. In some cases, the Data Team fixed tower locations that were 50-100 meters misplaced from the correct location. We also did not edit the operating voltage tag for the HV lines. If the voltage existed prior to the project start, we left it in place; otherwise, we did not add it.

Because it was difficult to keep track of which areas they had reviewed, the Data Team customized the [To-Fix plugin](https://wiki.openstreetmap.org/wiki/JOSM/Plugins/To-fix) available in JOSM. Rather than manually zoom and pan between each predicted tower, this allowed them to load in the ML-derived prediction map and iterate over individual predictions one at a time with the click of a button. This helped organize the review process and increased the speed of each mapper. The Data Team was tasked with tracing tower and power substation they could find (even if it was not identified in the ML portion of the pipeline). The GeoJSON overlay acted as a guide so that the mappers could efficiently hook into a section of the network and begin mapping, but it did not dictate all of their mapping efforts.

The Data Team went back and validated all edits once their initial mapping pass was complete. The goal was to double check for any missing connections and verify the accuracy of all added features (e.g., HV towers and substations). As edits were made within OSM itself, all additions were immediately available for anyone to view and access. We then computed final statistics on the mapping rate (in of km<sup>2</sup> per hour and towers per hour) during the generation of training data and during country-wide prediction (i.e., before and after the ML overlay was available). These two data points allowed us to calculate the relative speed of pure manual mapping and ML-assisted mapping.
