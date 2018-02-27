---
title: "Optimization: model training"
date: 2018-02-16
layout: post.html
---

To test many different combinations of model hyperparameters, we used the Hyperopt library and the tracked each model's performance in Tensorboard. The full list of possible hyperparameters is available in `config.py`, but some of the most important examples include the optimization scheme, learning rate, and non-linear activation function. By visualizing model loss and performance on the held-out test data (Figure 7), this allowed us to pick the highest performing model of about 150 models tested throughout the early stages of this project.


<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/tensorflow_results.png" alt="Tensorboard" />
  <figcaption><b>Figure 7. Validation loss and accuracy during training.</b> Each line represents the training of one model over time viewed in Tensorboard. Left: loss on the validation data (using binary cross-entropy on the probability output). Right: accuracy on the validation data as proportion of images correctly classified.</figcaption>
</figure>
