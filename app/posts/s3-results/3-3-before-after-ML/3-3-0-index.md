---
title: Mapping speed
date: 2018-02-16
layout: post.html
---

This project substatially expanded the amount of mapped HV infrastructure (Figure 13) including a more than four-fold increase in both Pakistan and Zambia. Edits include both additions and major corrections though the majority of edits were additions.

We found that our Data Team was approximately 33.4x faster per km<sup>2</sup> with the ML-derived overlay for Pakistan, Nigeria, and Zambia (Figure 14). The total time spent mapping and validating each country using these ML predictions is in Table 1.

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/mapped_features.png" alt="Total mapping edits." />
  <figcaption><b>Figure 13. HV infrastructure features in OSM. Left: Total number of HV towers at the conclusion of this project split up into existing (dark blue) and those edited during this project (either added or corrected; light blue). Right: Total number of substations at the conclusion of this project split up into existing (dark blue) and those edited during this project (light blue). In both, the large majority of edits were additions.</b></figcaption>
</figure>

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/mapping_rate.png" alt="Mapping rate for km^2, towers, and substations per hour." />
  <figcaption><b>Figure 14. Mapping rate with and without ML-assist.</b> On average, km<sup>2</sup> per hour increased by 33.4x, towers per hour by 9.7x, and substations per hour by 15.9x. Note that these figures exclude hours spent validating (i.e., double-checking) added edits. This ensured a fair comparison as no double-checking was carried out during the pre-ML mapping work to generate the training data.</figcaption>
</figure>

Table 1. **Total person-hours spent mapping at country-wide scale.**

| Country    | Hours mapping    | Hours validating |
|:---------- |:---------------- |:---------------- |
| Pakistan   | 364.13		    | 181.09 	 	   |
| Nigeria    | 243.12           | 74.47  		   |
| Zambia     | 167.17           | 29.45            |