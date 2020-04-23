# Credit_Risk_Assessment
Module 17

### 1. Oversample Using RandomOverSampler and SMOTE
    Random oversampling was practiced in two ways, one using RandomOverSampler which randomly chooses and adds instances from the minority class to the training set until the classes are balanced. SMOTE does this by creating new instances based on the values in clusters of the minority class.
    Random Oversampling resulted in a 65.4% Balanced Accuracy Score, "high_risk" Precision/Recall was .01 / .69 and "low_risk" Precision/Recall was 1.00 / .62. Though there was not a large disparity in the Recall scores, there was a major difference in precision. Precision for assessing high risk loans in this model is extremely low and low risk loan assesment was high. The sampling technique SMOTE had a similar outcome, the Balanced Accuracy Score was slightly higher at 66.2%. Precision was the same and the high_risk/low_risk recall was .63 / .69. Again this over sampling technique did well to assess low_risk scores, however very low precision identifying high_risk scores. 

### 2. Undersample Using Cluster Centroids
    Cluster Centroid Undersampling is a technique that asses clusters and creates a synthetic datapoint using the cluster values. The majority class is then undersampled to balance minority class. This technique was performed slightly lower than the oversampling technique. the Balanced Accuracy Score was 53.3%, Preciscion was .01/1.00, again poor identification of high_risk scores and Recall .66/.40, with a lowered recall of low_risk scores. 

### 3. Combination Sampling
    Combination sampling is a technique that oversamples the minority, then cleans up the resulting data by removing neighboring data points that belong to two different classes. In this instance, performance was improved in having the highest detection of True Positives and the recall value for high_risk detection was highest. 

### Model Choice
    There were small variances in each model, Cluster Centroid was probably the least successful and not recommended for use. While all models performed well in assessing loans that would be considered low risk, neither really performed well in detecting high risk loan applicants, which is the ideal goal. Combination Sampling is suggested because of the added complexity of cleaning nearest neighbors in differing classes, reducing the risk of reproducing data from the majority class and representing it as a minority value.