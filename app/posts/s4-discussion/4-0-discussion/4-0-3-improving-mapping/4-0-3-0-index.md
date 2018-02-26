---
title: Improving mapping workflow
date: 2012-08-23
layout: post.html
---

Machine learning aside, there is room for improvement on the human component of our mapping efforts carried out by the Data Team. The concept of using machine learning to guide mapping was new and untested for our professional mappers and our ML team, so we collected ideas to streamline the process throughout this project. Early on, our Data Team realized that navigating through the ML model's predictions was slow — initially they were repeatedly zooming in to map a few towers and then zooming out to reestablish a high-level view of the predictions. This constant reorientation of the view also made it difficult to keep track of which areas had been reviewed. As discussed in the Methods, the Data Team built its own To-Fix plugin within JOSM so they could click through the model's predictions with a single button.

Another limitation was that the ML predictions were not available to view in the tasking manager. Again, this is the piece of software that mappers regularly use to "lock" and then review small regions when a group of people is mapping the same larger area. Initially, there was no way to view the ML predictions in this overlay. Toward the middle of this project, we were also able to create the ability to add the ML overlay just like other map layers, so now the basic ML overlay appears in the tasking manager. 

The Data Team also noted that image quality varied across entire countries. In some cases, it was difficult to make accurate maps due to blurry or otherwise poor-quality imagery. In the future, we should explore other sources of data. Additionally, there were some cases where the network structure was ambiguous. For example, we found connections involving three HV towers, changes in the size (and possibly voltage) of HV towers, or areas where the HV lines appeared to bifurcate. In these special cases, we should explore the possibility of an engineering consult who is familiar with typical HV network construction.
