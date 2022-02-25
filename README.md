  # Credit_Risk_Analysis


## Overview of the Analysis

The purpose of this analysis was to analyze the relationship of multiple factors and their relation with the status of a loan.  The data provided had many columns of data.  Too many to even list here. Before assigning x and y, all column data types had to be converted to floats using the get_dummies() function. Next the data was split up into x and y. X being all columns excluding loan_status.  Y was the loan_status data.  This set up allowed for training certain models on the data.

![image](https://user-images.githubusercontent.com/85581208/155741718-459006de-640d-41f8-8d6f-eeda7e97ea57.png)


After assigning the data into the variables X and Y, it was divided into training and testing samples.  Image shows coding and sizes of each group.

![image](https://user-images.githubusercontent.com/85581208/155741442-d4a99da6-c8c8-4a54-b275-4dde43ab5a9a.png)


The first two models were oversampling algorithms, RandomOverSampler and SMOTE.  The next section included an undersampling algorithm, ClusterCentroids.  Lastly a combination over and under sampling algorithm was applied to the data, SMOTEENN.  The results and comparisons of these will be discussed below.  The last part of the analysis including boosting the data set with two ensemble learning algorithms, Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier.

## Results

Oversampling models
  -Naive Random
    -Balanced accuracy score = 0.649
    -Classification report = 
    ![image](https://user-images.githubusercontent.com/85581208/155741865-9b001738-d814-4174-bb8c-80858814eef5.png)
  
  
  The balanced accuracy score is ok but not great at 65%.  The reliability of the model is moderate.
  The average precision score is 0.99.  The average recall is 0.68.  The average f1 score is 0.80.
  
  -SMOTE
    -Balanced accuracy score = 0.644
    -Classification report = 
    ![image](https://user-images.githubusercontent.com/85581208/155746713-231749f5-3be3-4b2b-82ad-0efa8cf93810.png)
  
  The average precision score is 0.99.  The average recall is 0.66.  The average f1 score is 0.79
  
  Undersampling model
    -ClusterCentroids
      -Balanced accuracy score = 0.529
      -Classification report = 
      ![image](https://user-images.githubusercontent.com/85581208/155748444-ab7cac79-b6ee-4688-9ce4-6ab6fbf65fce.png)
      
      
    The average precision score is 0.99 and the recall score is 0.45.  The f1 is 0.62.
    
  Combination Sampling model
    -SMOTEENN
      -Balanced accuracy score = 0.637
      -Classification report
      ![image](https://user-images.githubusercontent.com/85581208/155749018-c485c9ce-8322-4266-a3fb-0afe36d0776f.png)
      
      
      
      The average precision score is 0.99 and average recall is 0.57.  The average f1 is 0.73.
      
      
      


    
    
    
