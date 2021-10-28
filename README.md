# Credit_Risk_Analysis

## Overview of the Analysis

This project applies machine learning to solve a real-world challenge: credit card risk.  We were able to employ different techniques to train and evaluate models with unbalanced classes.  We used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. We used the credit card dataset from LendingClub, a peer-to-peer lending services company to oversample the data using RandomOverSampler and SMOTE algorithms and undersample the data using the ClusterCentroids algorithm.  Next, we used a combinational approach of over and undersampling using the SMOTEENN algorithm.  Finally, we were able to compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.


## Results

- RandomOverSampler

![image](https://user-images.githubusercontent.com/64279232/137960163-1332cdff-89b9-4475-ab6a-21fddf2a1936.png)
![image](https://user-images.githubusercontent.com/64279232/137960228-a352634c-a1d8-4c7a-9f4e-30338b9bc782.png)

The high_risk precision is only about 1%, but overall average is 99% due to the low_risk population.  


- SMOTE

![image](https://user-images.githubusercontent.com/64279232/137960551-ff1a4cef-45f1-4bb9-9cd1-ccff7a75b118.png)

The SMOTE results are very similar to the RandomOverSampler model.  This model shows slightly more predicted high/actual low_risk compared to the last, making the recall slightly lower for the low_risk population. 


- ClusterCentroids

![image](https://user-images.githubusercontent.com/64279232/137960919-7bc4305f-bd63-420d-a2a6-a465fe6e8685.png)

The blanced accurary score has decreased in this model (54%).  This model also shows a high number of false positives (10,003) resulting in a low low_risk sensitify. 


- SMOTEENN

![image](https://user-images.githubusercontent.com/64279232/137961319-4b8f168c-494c-4a87-80b5-8a13941b9593.png)
![image](https://user-images.githubusercontent.com/64279232/137961369-b191d4ef-33e4-403b-a68d-f60d243a26a9.png)

The balanced accuracy score is now at 63%.


- BalancedRandomForestClassifier

![image](https://user-images.githubusercontent.com/64279232/137961600-81f79f41-3d23-4103-8678-8843da515469.png)

The balanced accuracy score is much higher with this model (79%), and the number of false positives is much lower (1560) creating a much higher overall sensitivity (91%).


- EasyEnsembleClassifier

![image](https://user-images.githubusercontent.com/64279232/137961876-6aeed848-b500-45ea-be38-e62aa1788c32.png)

This model has the highest balanced accuracy score (93%), precision of 99% and sensitivy of 94%.  



## Summary

Overall, I would recommend using the ensemble models, and more specifically, the EasyEnsembleClassifier due to the lower number of false positives and higher balanced accuracy score.  The banks will definitely need to keep in mind the possibility of low risk credits being falsely detected.  
