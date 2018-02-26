---
title: "Optimization: signal detection threshold"
date: 2018-02-16
layout: post.html
---

Because our model provides output in the form of a probability between zero and one, we can frame this problem with a perspective from signal detection theory. Signal detection provides theoretical guidance on how to select a threshold cutoff to designate which images are said to contain towers and which aren’t -- often there is a better choice than 0.5. Here, this threshold defines which tiles should be included in the map overlay provided to the data team. To better inform this decision threshold, we used ROC analysis from signal detection theory; an ROC curve provides insight into how our the true positive-rate (TPR) and false-positive rate (FPR) change with a changing threshold. For this problem, the TPR gives the proportion of tiles truly containing a HV tower that were selected by the ML model. The FPR is the portion of model selections that were incorrect (i.e., probability of a false alarm). We obtain an area under the curve (AUC) of 0.96 in held out data from the three train regions with a threshold=0.31 for the optimal minimum corner distance (Figure XXX). This indicates very high performance, but note that this is specific to data from the small training data set. When we ran this model at the country-wide scale, we noted a substantial drop in performance as explained in the discussion section.

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/roc_0129_052307.png" alt="ROC Curve" />
  <figcaption><b>Figure XXX. ROC curve for model’s performance on detecting HV towers.</b> </figcaption>
</figure>

We can also visualize the score distributions themselves for the held-out data in the training set.

<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/dist_fpr_tpr_0129_052307.png" alt="Model’s assigned probabilities for images containing and not containing HV towers." />
  <figcaption><b>Figure XXX. Assigned probability distributions for images containing (red) and not containing (blue) HV towers.</b> The model’s assigned probability scores (x-axis) are displayed as an estimated probability density function (with probability on the y-axis). Note that the model is able to properly separate the majority of images in this validation data.</figcaption>
</figure>
