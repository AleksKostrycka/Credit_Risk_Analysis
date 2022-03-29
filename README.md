# Credit_Risk_Analysis
## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, i will need to employ different techniques to train and evaluate models with unbalanced classes. I have been asked to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once completed, I will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

### RandomOverSampler Model

![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/OverSampling%20Model.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/oversampling2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/oversampling3.png?raw=true)

The results above indicate the balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
The low_risk precision is almost 100% with a sensitivity of 68%. 

### SMOTE Model
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel3.png?raw=true)

The results above indicate a balanced accuracy score is 64%.
The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
The low_risk precision is almost 100% with a sensitivity of 66%. 

### ClusterCentroids model
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroidsmodel.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroidsmodel2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroidsmodel3.png?raw=true)

Here the balanced accuracy score is down to about 53%.
The high_risk precision is still 1% only with 61% sensitivity which makes a F1 of 1%.
The low_risk precision is almost 100% with a sensitivity of 45%. 

### SMOTEEN Model
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smoteenmodel.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smoteenmodel2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smoteenmodel3.png?raw=true)

The balanced accuracy score is about 62%.
The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.
The low_risk precision is almost 100% with a sensitivity of 57%. 

### BalancedRandomForestClassifier model
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/balancedradnomforestclass.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/balancedrandomforestclass2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/balancesrandomforestclass3.png?raw=true)

The balanced accuracy score improved to about 79%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
The low_risk sensitivity is 91% with 100% presicion. 

### EasyEnsembleClassifier model

![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/easyensambleclassifier.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/easyensambleclassifier2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/easyensambleclassifier3.png?raw=true)

The balanced accuracy score is about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
The low_risk sensitivity is now 94% with 100% presicion. 

## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought more improvment on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 93% so it detects almost all high risk credit. However, with low precision it indicates that a lot of low risk credits are still falsely detected as high which would penalize the bank's credit strategy. The model says that it is missing out on revenue by not including those business opportunities (low risk being falsely detected as high risk).
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
