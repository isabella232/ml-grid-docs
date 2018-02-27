---
title: Discussion and future directions
date: 2012-08-23
layout: post.html
---

We created a workflow to boost human mapping speed by 15-20x when tracing high-voltage infrastructure. At a high level, we used machine learning to find satellite imagery tiles that were most likely to contain HV towers and then pass this information to our Data Team -- a group of professional mappers -- to trace the HV infrastructure. This strategy was testing in three countries: Pakistan, Nigeria, and Zambia comprised of a total land area of XXX km^2.

Throughout the course of this project, we confirmed that neither humans nor an automated system alone are currently a feasible approach for mapping HV infrastructure. One one hand, professional mappers are very accurate and know when to ask for confirmation on difficult imagery. However, the time required to manually review an entire country is tremendous. We estimated it would have taken our Data Team about 6 months of full time effort to complete Pakistan. On the other hand, ML algorithms can operate with very high throughput and very little oversight once trained. Pakistan required only several days of computation time and a few hours of human effort to monitor the scripts. Nevertheless, our ML results indicated that it would be practically impossible to train an algorithm as accurate as a human. Combining them in an Intelligence Augmentation (IA) approach leveraged the strengths of both humans and machines.

The IA approach is also prudent in comparison to a pure AI strategy focused on completely replacing humans. By keeping a human in the loop, we can make sure all ML predictions are validated by a professional mapper before the additions are incorporated into OSM. The OSM community is (rightly) skeptical of any method that add edits without human verification as this strategy has led to issues in the past. Therefore, building a workflow utilizing the strengths of both is likely the optimal way forward. Future work should focus on improving the machine learning predictions and better incorporating those predictions into mapping editors (perhaps as plugins for standard map editors) so they are widely available to human mappers.


## Future directions
The rest of this discussion section is focused on improvements for future iterations of this mapping workflow.

1. **Improving how we handle big data**
    1. Efficiently downloading and storing large imagery datasets
    1. Matching download and prediction speeds on the fly
1. **Improving the machine learning predictions**
    1. Detecting HV substations
    1. Improving HV tower detection
    1. Using additional forms of imagery (like SAR)
1. **Integrating ML predictions into human mapping workflows more effectively**
