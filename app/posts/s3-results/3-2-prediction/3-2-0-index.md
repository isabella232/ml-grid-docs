---
title: Country-wide predictions
date: 2018-02-16
layout: post.html
---

After selecting an optimal model and an appropriate decision threshold, we processed imagery across Pakistan, Nigeria, and Zambia. Here, the same model was used across all three countries. In general, we found (unsurprisingly) that the model performed much better in regions where we collected the original training data likely because of the similar terrain.

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_pakistan_2.png" alt="Pakistan country-wide HV tower prediction" />
  <figcaption><b>Figure XXX. Country-wide prediction map in Pakistan.</b> Black dots correspond to locations where the model predicts a HV tower was present. In the mountainous desert region of Pakistan, the model performed relatively well. In the Eastern agricultural region, the model predicted many more false positives as we did not obtain any training data from this region.</figcaption>
</figure>

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_nigeria_1.png" alt="Nigeria country-wide HV tower prediction" />
  <figcaption><b>Figure XXX. Country-wide prediction map in Nigeria.</b></figcaption>
</figure>

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_zambia_1.png" alt="Zambia country-wide HV tower prediction" />
  <figcaption><b>Figure XXX. Country-wide prediction map in Zambia.</b></figcaption>
</figure>
