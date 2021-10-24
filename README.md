# Credit_Risk_Analysis

## Overview of the analysis:
The purpose of this analysis was to create six different models to determine which model should be used to predict credit risk. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we ran RandomOversampling, SMOTE Oversampling, ClusterCentroids resampler, SMOTEENN, BalancedRandomForestClassifier and EasyEnsembleClassifier models to see which one was best at predicting the credit risk of the lending service data.

## Results: 

   ### RandomOversampling
   
      The accurancy of oversampling the data was 0.65, which is not the best.
      High_risk has a very low precision of only 1% and only recalled 73% of actual high risk loans.
      
   ![Random Oversampler](https://user-images.githubusercontent.com/84158312/138611921-149faf17-8123-449f-8f08-f2886fb1cec1.png)
    
   ### SMOTE
   
      SMOTE is another oversampling technique. This model was also only 66% accurat. 
      The SMOTE model also had only a 1% precision rate and then a recall of 63% for the High_risk loans.
   
   ![SMOTE Oversampling](https://user-images.githubusercontent.com/84158312/138611926-dd647b58-b9cb-417a-bef2-5f6f6947560a.png)

   ### ClusterCentroids
   
      ClusterCentroids is an undersampling model. The accurancy for this model for this data was 58%.
      For high risk loans, the precision was 1% and the recall rate was 67%.
   
   ![Random Undersampler](https://user-images.githubusercontent.com/84158312/138612022-df6b8c98-0ca4-45e7-b00c-2f25545281d4.png)

   ### BalancedRandomForestClassifier
   
      This model has the highest accurancy out of all the previous models of 78%.
      This probably has to do with the precision of the classification report being 3% rather than 1%. The recall rate however was 67%.
   
   ![Balanced Random Forest](https://user-images.githubusercontent.com/84158312/138611952-4062c40c-3388-4083-83cf-c057cfff9371.png)

   ### SMOTEENN
   
      SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms, oversampling the minority of the sample, plotting it and then nullfying the datapoint if the nearest neighbors of a data point belong to two different classes. The accurancy of this model was 65%, similar to the other models. The precision was 1%, like most of the models and with a recall rate of 72%.
   
   ![SMOTEENN model](https://user-images.githubusercontent.com/84158312/138611933-b30f05f6-3776-4603-aaf4-4b454fc14664.png)
   
   
  ### EasyEnsembleClassifier
   
      This model has the highest accuracy of all the models of 93%.
      Ther precision of this model was 9%, also the highest as well as as recall rate of 92%.
   
   ![Easy Ensemble](https://user-images.githubusercontent.com/84158312/138612041-4b2bd7ab-3115-4e27-abdc-3be6d19d095b.png)


## Summary:

After reviewing the accurancy, precision and recall rates of all the models, the easyEnsembleClassifier had the highest of all three factors out of the 6 models we tested. The Easy Ensemble creates balanced samples of the training dataset by selecting all examples from the minority class and a subset from the majority class, and running these over and over while impoving itself each time. This is probably why it was the most accurate and precise. I would recommend to use this model and keep improving it and the data collected to have the most accurate and precise model.
