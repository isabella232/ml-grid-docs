---
title: Compute costs
date: 2018-02-16
layout: post.html
---

All computation and data manipulation was carried out on Amazon Web Services (AWS). We used AWS Elastic Compute Cloud (EC2) for the model training and prediction. Here, we primarily used the `p2.xlarge` instances, which contain GPUs suitable for deep learning. To download the satellite imagery from the Digital Globe Maps API, we used `m5.xlarge` and `c5.9xlarge` instances as these could handle large numbers of threads making the necessary HTTP requests. To store the data, we used AWS Simple Storage Service (S3). Note that the below costs do not include any associated imagery costs. Those are difficult to estimate because of the unique contracts each organization makes with satellite imagery providers. The total compute cost was $1,137.85 or about $0.42 per 1,000 km<sup>2</sup>. A more-detailed compute cost analysis is available in Table 2.

**Table 2. Costs for obtaining, storing, and processing satellite imagery**
| Service        					      | Cost           |
|:--------------------------------------- | --------------:|
| AWS EC2: downloading imagery  	      |  $59.38 	   |
| AWS EC2: training and predicting        | $392.14 	   |
| AWS S3: storing and accessing imagery   | $686.33 	   |
| **Total**							      | **$1137.85**   |
