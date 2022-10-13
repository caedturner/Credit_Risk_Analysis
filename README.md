# Credit_Risk_Analysis

### Overview
The goal of this analysis is to look at credit card applicant data and detirmine the risk assumed if the credit card company issues an account. I applied Machine Learning in different forms to best form a conclusion based on the data given.

### Analysis

1. RandomOverSampler
  - Balanced Accuracy Report - 0.6620355148236994
  - Precision - High risk: 0.01, Low Risk: 1.00
  - Due to the sample imbalance the model preformed at a low Balanced Accuracy rate as well as a very skewed precision rate. 
<img width="295" alt="Screen Shot 2022-10-12 at 22 33 29 PM" src="https://user-images.githubusercontent.com/106132054/195510084-95a94952-038b-4052-8eff-eb45bcdb31b9.png">
<img width="218" alt="Screen Shot 2022-10-12 at 22 33 40 PM" src="https://user-images.githubusercontent.com/106132054/195510109-28cc7c40-d773-4ea6-9a61-2080c221d3dc.png">


2. SMOTE
  - Balanced Accuracy Report - 0.6620355148236994
  - Precision - High risk: 0.01, Low Risk: 1.00 
  - This model preformed at the same quality as the RandomOverSampler
<img width="277" alt="Screen Shot 2022-10-12 at 22 33 05 PM" src="https://user-images.githubusercontent.com/106132054/195510030-b4df627d-bf59-4c2a-a72d-9b9a3dfd0047.png">
<img width="231" alt="Screen Shot 2022-10-12 at 22 33 17 PM" src="https://user-images.githubusercontent.com/106132054/195510056-5d565a95-b867-48ad-b35c-c00a7d6ccc58.png">


3. Cluster Centroids
  - Balanced Accuracy Report - 0.5447339051023905
  - Precision - High risk: 0.01, Low Risk: 1.00 
  - This model preformed even poorer than the first two in terms of the accuracy, though the precision was the same. Keep in mind this data is heavily skewed.
<img width="291" alt="Screen Shot 2022-10-12 at 22 32 30 PM" src="https://user-images.githubusercontent.com/106132054/195509982-243b051f-e7bc-46b9-8be7-951de8d3d5b6.png">
<img width="230" alt="Screen Shot 2022-10-12 at 22 32 44 PM" src="https://user-images.githubusercontent.com/106132054/195509989-9cc2f5d2-12bf-4b2f-9597-39deff4696e5.png">


4. SMOOTEENN
  - Balanced Accuracy Report - 0.5447339051023905
  - Precision - High risk: 0.01, Low Risk: 1.00 
  - Similar to the Cluster Centroids performance.
<img width="266" alt="Screen Shot 2022-10-12 at 22 31 37 PM" src="https://user-images.githubusercontent.com/106132054/195509855-3f3c0e87-1004-4128-ad9f-e59852fd3cc0.png">
<img width="221" alt="Screen Shot 2022-10-12 at 22 31 43 PM" src="https://user-images.githubusercontent.com/106132054/195509868-2281cc11-339a-4e8a-a46a-46eabc00b5da.png">


5. BalancedRandomForestClassifier
  - Balanced Accuracy Report - 0.7885466545953005 
  - Precision - High risk: 0.03, Low Risk: 1.00 
  - This model has the best over all accuracy as well as ability to predict the high risk - which is a drastically skewed metric. 
<img width="304" alt="Screen Shot 2022-10-12 at 22 31 02 PM" src="https://user-images.githubusercontent.com/106132054/195509769-163158c4-5366-4607-9e9a-dd30d96ab6ee.png">
<img width="226" alt="Screen Shot 2022-10-12 at 22 31 08 PM" src="https://user-images.githubusercontent.com/106132054/195509782-0057ac0f-4f43-4973-813c-419bf82b69f0.png">


6. EasyEnsembleClassifier
  - Balanced Accuracy Report - 0.773197051931573
  - Precision - High risk: 0.04, Low Risk: 1.00 
  - This model has the second highest accuracy report and a better brecision on the high risk metric than all the others.
<img width="287" alt="Screen Shot 2022-10-12 at 22 30 20 PM" src="https://user-images.githubusercontent.com/106132054/195509669-f9d7f8d4-2cdb-4fbd-a284-f5a660257b32.png">
<img width="224" alt="Screen Shot 2022-10-12 at 22 30 25 PM" src="https://user-images.githubusercontent.com/106132054/195509680-01e4c30c-494d-4913-9e0d-30483810162e.png">

### Summary
The results of all tested models show that there is a fairly poor overall Balanced Accuracy report - 0.7885466545953005 being the highest - which could be enhanced substantially by simply stabalizing the data. The best performing precision score is very low for the high risk metric - 0.04 - which can also be helped by stabalizing the data and making it more uniform. I would choose to stabalize the data and use the Balanced Random Forest Classifier model to try to make as good of predictions as possible.
