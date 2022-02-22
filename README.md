  # Credit_Risk_Analysis


## Overview of the Analysis

The purpose of this analysis was to analyze the relationship of multiple factors and their relation with the status of a loan.  The data provided had many columns of data.  Too many to even list here. Before assigning x and y, all column data types had to be converted to floats using the get_dummies() function. Next the data was split up into x and y. X being all columns excluding loan_status.  Y was the loan_status data.  This set up allowed for training certain models on the data.

The first two models were oversampling algorithms, RandomOverSampler and SMOTE.  The next section included an undersampling algorithm, ClusterCentroids.  Lastly a combination over and under sampling algorithm was applied to the data, SMOTEENN.  The results and comparisons of these will be discussed below.  The last part of the analysis including boosting the data set with two ensemble learning algorithms, Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier.

## Results
