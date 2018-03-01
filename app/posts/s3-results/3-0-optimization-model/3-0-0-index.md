---
title: "Optimization: model training"
date: 2018-02-16
layout: post.html
---

When training deep learning models, there are many small choices to make regarding the architecture and training procedure to follow. Typically, a good strategy is to test a wide range of hyperparameters and select the model with the highest performance. The full list of possible hyperparameters is available in `config.py`, but some of the most important examples include the optimization scheme, learning rate, and non-linear activation function. To automate testing process, we used the Hyperopt library and the tracked each model's performance in Tensorflow's Tensorboard -- a tool for visualizing model performance during training (Figure 7). We tested about 150 different iterations of the Xception model during the early stage of this project and selected the highest performing one.


<figure class="align-center">
  <img src="/assets/graphics/content/results_plots/tensorflow_results.png" alt="Tensorboard" />
  <figcaption><b>Figure 7. Validation loss and accuracy during training.</b> Each line represents the training of one model over time viewed in Tensorboard. Left: loss on the validation data (using binary cross-entropy on the probability output) where lower is better. Right: accuracy on the validation data as proportion of images correctly classified. Here, higher is better.</figcaption>
</figure>