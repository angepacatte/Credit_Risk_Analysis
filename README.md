  # Credit_Risk_Analysis


## Overview of the Analysis

The purpose of this analysis was to analyze the relationship of multiple factors and their relation with the status of a loan.  The data provided had many columns of data.  Too many to even list here. Before assigning x and y, all column data types had to be converted to floats using the get_dummies() function. Next the data was split up into x and y. X being all columns excluding loan_status.  Y was the loan_status data.  This set up allowed for training certain models on the data.

![image](https://user-images.githubusercontent.com/85581208/155741718-459006de-640d-41f8-8d6f-eeda7e97ea57.png)


After assigning the data into the variables X and Y, it was divided into training and testing samples.  Image shows coding and sizes of each group.

![image](https://user-images.githubusercontent.com/85581208/155741442-d4a99da6-c8c8-4a54-b275-4dde43ab5a9a.png)


The first two models were oversampling algorithms, RandomOverSampler and SMOTE.  The next section included an undersampling algorithm, ClusterCentroids.  Lastly a combination over and under sampling algorithm was applied to the data, SMOTEENN.  The results and comparisons of these will be discussed below.  The last part of the analysis including boosting the data set with two ensemble learning algorithms, Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier.

## Results

Oversampling Models
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
  
  Undersampling Models
    -ClusterCentroids
      -Balanced accuracy score = 0.529
      -Classification report = 
      
      ![image](https://user-images.githubusercontent.com/85581208/155748444-ab7cac79-b6ee-4688-9ce4-6ab6fbf65fce.png)
      
      
    The average precision score is 0.99 and the recall score is 0.45.  The f1 is 0.62.
    
  Combination Sampling Models
    -SMOTEENN
      -Balanced accuracy score = 0.637
      -Classification report
      
      ![image](https://user-images.githubusercontent.com/85581208/155749018-c485c9ce-8322-4266-a3fb-0afe36d0776f.png)
      
      
      
      -The average precision score is 0.99.
      -The average recall is 0.57.  
      -The average f1 is 0.73.
      
   Ensemble Learner Models
    -Balanced Random Forest Classifier
      -Balanced accuracy score = 0.787
      - Classification report
      
      ![image](https://user-images.githubusercontent.com/85581208/155750699-656fed55-7fd7-4b14-8aed-e5c2ed94973a.png)
      
      
      
      -The average precision score is 0.99. 
      -Average recall is 0.91.  
      -The average f1. 0.95.
      
    
    
    -Easy Ensemble AdaBoost Classifier
      -balanced accuracy score = 0.925
      - Classification report
      
      ![image](https://user-images.githubusercontent.com/85581208/155750990-ae344d86-5f34-4300-9e0b-44c33c84e111.png)


      -The average precision score is 0.99 as in all models
      -The average recall is 0.94.
      -The average f1 is 0.97.
      
      
      ## Summary
      
      After assessing all 6 models, the two ensemble learner models are the best fits for the data. The Easy Ensemble Classfier is the best of thos two. It is a good balance of accuracy an sensitivity.  The f1 score of 0.97 shows the test.  The sensitivity and precision are very accurate.  This is also reflected in the accuracy score of 0.925. 
      The balanced ranadom forest classifier had a lower accuracy score of 0.787.  The f1 score was only slightly lower at 0.95.  These models specificity are the best.  Not only are they senstive in assessing high risk loans.  They are accurate.
        The least accurate model was ClusterCentroids undersampling model.  Accuracy score of 0.529 and f1 is 0.62.  The other models were under 0.8 for the f1 score which is a good measure of both precision and recall.  The closer to 1 the f1 score is the better the model is in sensitivity and specificity together.

      
      
      
      
      


    
    
    
