---
title: Executive Summary
date: 2018-02-16
layout: post.html
permalink: /
---

Many people in the world still do not have access to electricity. In developing nations, this problem is especially acute as it limits participation in modern economy and culture. Improving the electric grid, however, is often logistically challenging in these regions because there is rarely a complete and accurate map of the existing electric infrastructure. This map is crucial as there is no way to make informed decisions on how to spend resources to improve the electric grid without it.

Toward solving this problem, we built a pipeline to efficiently map the high-voltage (HV) grid at a country-wide scale. This pipeline relied on both machine learning (ML) and our Data Team -- a group of eight professional mappers. The ML component processes satellite imagery across an entire target country and returns geospatial locations likely to contain HV towers -- the tall metal structures that support HV lines running for hundreds or thousands of kilometers. Our Data Team then overlaid this information on top of satellite imagery within their mapping workflow. With this overlay, they focused their efforts on tracing HV towers, lines, and substations and were able to avoid the brute-force approach of manually checking every meter of ground. 

Using this pipeline, we mapped nearly all of the HV network in Pakistan, Nigeria, and Zambia and found that our ML model [increase mapping speed **33-fold**](http://devseed.com/ml-grid-docs/results/mapping-output-and-speed) per km<sup>2</sup> compared to a purely manual approach. Examples of satellite images and the final workflow are below. The [model, code, and mapping output are openly available](https://github.com/developmentseed/ml-hv-grid-pub), and we outline possibilities for further improvements of this pipeline in the Discussion section.

<figure class="align-center">
  <img src="/assets/graphics/content/hv_grid_tower_tracing.gif" alt="Tracing HV towers." />
  <figcaption><b>Figure 1. Tracing with ML-derived prediction overlay.</b> Each square represents a tile that the ML model believed to contain a HV tower. The Data Team then mapped from tower to tower using this overlay as a guide. Video reflects actual speed.</figcaption>
</figure>

