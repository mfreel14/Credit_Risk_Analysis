# Credit Risk Analysis

## Project Overview - Credit Risk Analysis

 With our LoanStats CSV data, we'll apply machine learning to understand credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.  To solve for this we'll employ different techniques to train and evaluate models with unbalanced classes. For the project we'll use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

With the credit card dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Then, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. THe results from the performance of these models will help us make a written recommendation on whether they should be used to predict credit risk.

## Resources
-  Data Files:  LedningClub - LoanStats_2019Q1.zip

-  Software/Languages:  Python 3.7.10, Anaconda Navigator, Conda, Jupyter Notebook 6.4.3, Pandas 1.2.4

# Challenge Summary

## Credit Risk Analysis - Results

## Credit Risk Resampling

### Naive Random Oversampling

![Screen Shot 2021-10-21 at 4 37 41 PM](https://user-images.githubusercontent.com/691355/138371048-37ebabaf-0050-45fb-b63b-675851abba06.png)

-  Accuracy Score: 65%
-  Precision High Risk: 1%
-  Precision Low Risk: 100%
-  Recall High Risk:  62% 
-  Recall Low Risk:  68%

### SMOTE Oversampling

![Screen Shot 2021-10-21 at 4 43 45 PM](https://user-images.githubusercontent.com/691355/138371479-9e4e8913-500a-4dcc-bc64-d4639b4ecef1.png)

-  Accuracy Score: 64%
-  Precision High Risk: 1%
-  Precision Low Risk: 100%
-  Recall High Risk:  63% 
-  Recall Low Risk:  66%

### Cluster Centroid Undersampling

![Screen Shot 2021-10-21 at 4 45 13 PM](https://user-images.githubusercontent.com/691355/138371594-bfbb0d53-16ea-4e4d-a0fd-468d995ecf1d.png)

-  Accuracy Score: 53%
-  Precision High Risk: 1%
-  Precision Low Risk: 100%
-  Recall High Risk:  61% 
-  Recall Low Risk:  45%

### SMOTEENN Sampling

![Screen Shot 2021-10-21 at 4 48 03 PM](https://user-images.githubusercontent.com/691355/138371835-3aaaa4ab-d7a8-409d-b18c-7f8e2d9b442f.png)

-  Accuracy Score: 62%
-  Precision High Risk: 1%
-  Precision Low Risk: 100%
-  Recall High Risk:  68% 
-  Recall Low Risk:  57%

## Credit Risk Ensemble

### Balanced Random Forest Classifier

![Screen Shot 2021-10-21 at 5 06 41 PM](https://user-images.githubusercontent.com/691355/138373174-c2fcc6cf-33ce-45c3-aa91-8ed412cb5a28.png)

-  Accuracy Score: 79%
-  Precision High Risk: 4%
-  Precision Low Risk: 100%
-  Recall High Risk:  67% 
-  Recall Low Risk:  91%

### Easy Ensemble AdaBoost Classifier

![Screen Shot 2021-10-21 at 4 52 02 PM](https://user-images.githubusercontent.com/691355/138372137-f01e4f18-26b9-4adc-80a7-24b93b084361.png)

-  Accuracy Score: 93%
-  Precision High Risk: 7%
-  Precision Low Risk: 100%
-  Recall High Risk:  91% 
-  Recall Low Risk:  94%


## Credit Risk Analysis - Summary

The models demonstrated in the credit risk resampling were random oversampling, SMOTE oversampling, cluster centroid undersampling and SMOTEENN sampling.  These models and the models used in the credit risk ensemble (BRFC and EEAC) were used to identify which loans were the highest risk.  

The three models with the highest recall rate for high risk were:
1.  Easy Ensemble AdaBoost Classifier - 91%
2.  SMOTEENN Sampling - 68%
3.  Balanced Randomd Forest Classifier

The three models with the highest recall rate for low risk were:
1.  Easy Ensemble AdaBoost Classifier - 94%
2.  Balanced Randomd Forest Classifier - 91%
3.  Naive Random Oversampling - 68%

The three models with the highest accuracy scores were:
1.   Easy Ensemble AdaBoost Classifier - 93%
2.   Balanced Randomd Forest Classifier - 79%
3.   Naive Random Oversampling - 65%


Taking these three statistics into account, I would recommend the Easy Ensemble Classifier model as the best predictor for high risk loans.

