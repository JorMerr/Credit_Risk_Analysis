# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis
The purpose of this loan prediction risk analysis is to determine the most suitable supervised machine learning model for predicting credit risk.
The analysis will cover two oversampling algorithms, RandomOverSampler and SMOTE; one undersampling algorithm, ClusterCentroids; one combinatorial algorithm, SMOTEENN;
and two new machine learning models for reducing bias, BalancedRandomForestClassifier and EasyEnsembleClassifier. Each model will be trained using input data from a credit card dataset from LendingClub, a peer-to-peer lending services company. 

The analysis will compare the results of each model's accuracy score, precision, and recall. This report will summarise the results and make a determination of which model, if any, is best suited to be used for predicting credit risk.

## Results of Analysis
As can be seen in the following breakdown of the results, the initial accuracy, precision, and recall scores for the dataset are:
- 
### Random Over Sampler
![ROS Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_Initial_and_naiveoversampling.JPG)

![ROS Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_naiveoversampling.JPG)

![ROS Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_naiveoversampling.JPG)

### SMOTE
![SMOTE Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_smote.JPG)

![SMOTE Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_smote.JPG)

![SMOTE Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_smote.JPG)

### Cluster Centroids
![CC Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_cc.JPG)

![CC Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_cc.JPG)

![CC Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_cc.JPG)

### SMOTEENN
![SMOTEENN Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_comb.JPG)

![SMOTEENN Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_comb.JPG)

![SMOTEENN Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_comb.JPG)

### Balanced Random Forest Classifier
![BRF Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_brf.JPG)

![BRF Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_brf.JPG)

![BRF Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_brf.JPG)

### Easy Ensemble Classifier
![EEC Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_eec.JPG)

![EEC Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_eec.JPG)

![EEC Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_eec.JPG)

## Summary