---
title: Compute Costs
date: 2018-02-16
layout: post.html
---

All computation and data manipulation was carried out on Amazon Web Services (AWS). We used AWS Elastic Compute Cloud (EC2) for the model training and prediction. Here, we primarily used the `p2.xlarge` instances, which contain GPUs suitable for deep learning. To download the satellite imagery from Mapbox's servers, we used `m5.xlarge` and `c5.9xlarge` instances as these could handle large numbers of threads making the necessary HTTP requests. To store the data, we used AWS Simple Storage Service (S3). Note that we were able to obtain all imagery from Mapbox free of charge for this project due to a special relationship with their company, but any future rounds of HV mapping would likely require these costs to be covered. In the end, the total compute cost was $1137.85 or about $0.42 per 1000 km^2. A more-detailed compute cost analysis is available in Table 2.

**Table 2. Costs for obtaining, storing, and processing satellite imagery**
| Service        					      | Cost           |
|:--------------------------------------- | --------------:|
| AWS EC2: downloading imagery  	      |  $59.38 	   |
| AWS EC2: training and predicting        | $392.14 	   |
| AWS S3: storing and accessing imagery   | $686.33 	   |
| Mapbox: imagery access 				  | $0	    	   |
| **Total**							      | **$1137.85**   |