---
title: Country-wide predictions
date: 2018-02-16
layout: post.html
---

After selecting an optimal model and decision threshold, we processed country-wide imagery sets across Pakistan, Nigeria, and Zambia (Figures 13-15). Note the thin snaking lines in these plots indicating where HV lines exist. The same model was used across all three countries, and we found (unsurprisingly) that the model performed much better in regions of each country where we collected the original training data (likely because of the similar terrain). Outside of these areas, the model gave more false positives (appearing as large dark blobs).

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_pakistan_2.png" alt="Pakistan country-wide HV tower prediction" />
  <figcaption><b>Figure 13. Country-wide prediction map in Pakistan.</b> Black dots correspond to locations where the model predicts a HV tower was present. In the mountainous desert region of Pakistan, the model performed relatively well. In the Eastern agricultural region, the model predicted many more false positives as we did not obtain any training data from this region.</figcaption>
</figure>

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_nigeria_1.png" alt="Nigeria country-wide HV tower prediction" />
  <figcaption><b>Figure 14. Country-wide prediction map in Nigeria. </b>The model made many false positives along the central savannah region of Nigeria. Here, the landscape is mostly comprised of exposed rock outcroppings and sharp hills. These rugged areas have many long cracks and grey-colored rocks that likely contributed to the false positives here. Our training data came from a very different terrain -- the tropical rainforest region in the Southeast.</figcaption>
</figure>

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/ml_output_zambia_1.png" alt="Zambia country-wide HV tower prediction" />
  <figcaption><b>Figure 15. Country-wide prediction map in Zambia.</b> The model performed relatively well in here -- likely the best of the three countries. In the Southern region, however, the imagery quality was relatively poor (i.e., somewhat discolored and blurry) compared to the rest of the country causing more false positive predictions. This is often indicated by sharp boundaries in prediction density. The effects of wildfires are also visible in some regions where the model performed poorly. This likely occurred because our training data did not sample from these burned regions. </figcaption>
</figure>
