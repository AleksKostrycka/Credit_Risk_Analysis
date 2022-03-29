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
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%. 

### SMOTE Model
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel2.png?raw=true)
![This is an image](https://github.com/AleksKostrycka/Credit_Risk_Analysis/blob/main/Resources/smotemodel3.png?raw=true)

The results above indicate a balanced accuracy score is 64%.
The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%. 

![This is an image]()
![This is an image]()
![This is an image]()

![This is an image]()
![This is an image]()
![This is an image]()

![This is an image]()
![This is an image]()
![This is an image]()

![This is an image]()
![This is an image]()
![This is an image]()
