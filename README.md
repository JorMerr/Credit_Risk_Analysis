# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis
The purpose of this loan prediction risk analysis is to determine the most suitable supervised machine learning model for predicting credit risk.
The analysis will cover two oversampling algorithms, RandomOverSampler and SMOTE; one undersampling algorithm, ClusterCentroids; one combinatorial algorithm, SMOTEENN;
and two new machine learning models for reducing bias, BalancedRandomForestClassifier and EasyEnsembleClassifier. Each model will be trained using input data from a credit card dataset from LendingClub, a peer-to-peer lending services company. 

The analysis will compare the results of each model's accuracy score, precision, and recall. This report will summarise the results and make a determination of which model, if any, is best suited to be used for predicting credit risk.

## Results of Analysis
As can be seen in the following breakdown of the results, the initial accuracy scores for the dataset are:
- Training: 67.89%
- Testing: 68.35%

The confusion matrix has been provided for each model to illustrate the actual vs predicted values.
### Random Over Sampler
- The Random Over Sampler model shows poorer performance than the initial training data with a Balanced Accuracy Score of **62.93%**. This value may be a result of the oversampling model creating datapoints weighted by outliers in the minority scores from the original data.
    - ![ROS Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_Initial_and_naiveoversampling.JPG)

- This model is more inclined to predict high credit risk when there is none, providing a statistically signigicant number of False Positives.
    - ![ROS Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_naiveoversampling.JPG)

- As show below, the Random Over Sampler model has a strong precision of accurately predicting low credit risk, but a very weak precision of predicting high credit risk.
- The recall for credit risk from this model shows that the probability of predicting low credit risk is weak at **68%**, and the probability of predicting high credit risk is only marginally better than 50% odds, at **57%**.
    - ![ROS Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_naiveoversampling.JPG)

### SMOTE
- We can see with SMOTE that the accuracy of our model is lower than Random Over Sampling, with a score of **62.77%**.
    - ![SMOTE Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_smote.JPG)

- This model again is more inclined to predict high credit risk where there is none, providing a statistically signigicant number of False Positives.
    - ![SMOTE Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_smote.JPG)

- Similar to the Random Over Sample model, the precision of predicting low credit risk is very strong, while the precision of predicting high credit risk is very low.
- The recall has increased to **62%** for the probability of predicting high credit risk, while the recall has decreased to **63%** for the probablity of predicting low credit risk.
    - ![SMOTE Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_smote.JPG)

### Cluster Centroids
- The ClusterCentroids model indicates a further decrease in accuracy, with a score of **51.03%**.
    - ![CC Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_cc.JPG)

- This model continues to be inclined to predict high credit risk where there is none, to the detriment of accurately predicting low credit risk. This results in a highly significant number of False Positives.
    - ![CC Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_cc.JPG)

- We see with ClusterCentroids a very low precision of accurately predicting high credit risk.
- The recall has decreased for both high and low credit risk predictions to **59%** and **43%** respectively.
    - ![CC Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_cc.JPG)

### SMOTEENN
- Using SMOTEENN to model a combinatorial approach, this model improves its accuracy score to **61.97%**.
    - ![SMOTEENN Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_comb.JPG)

- This model continues to be inclined to predict high credit risk where there is none, resulting in a high number of False Positives.
    - ![SMOTEENN Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_comb.JPG)

- SMOTEENN has a very low precision of accurately predicting high credit risk.
- Overall, the combinatorial approach of SMOTEENN has improved the high credit risk recall scores with **70%** recall for high credit risk, and **54%** recall for low credit risk when compared to over or undersampling models on their own.
    - ![SMOTEENN Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_comb.JPG)

### Balanced Random Forest Classifier
- Our Ensemble learning models show higher performance than the resampled models. BalancedRandomForestClassifier shows an accuracy score of **87.35%**.
    - ![BRF Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_brf.JPG)

- While still indicating a number of False Positives, this model has more accurately predicted high credit risk than previous models.
    - ![BRF Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_brf.JPG)

- BalancedRandomForestClassifier continues to have a low precision of predicting high credit risk.
- This model has much improved recall of accurately predicting high credit risk and low credit risk, with recall scores of **70%** and **87%** respectively.
    - ![BRF Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_brf.JPG)

### Easy Ensemble Classifier
- The EasyEnsembleClassifier model appears to be similarly accurate to the BalancedRandomForestClassifier model, with an accuracy score of **87.35%**
    - ![EEC Balanced Accuray Score](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/acc_score_eec.JPG)

- This model has shown the lowest number of False Positives predicted. 
    - ![EEC Confusion Matrix](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/cm_eec.JPG)

- EasyEnsembleClassifier had a weak precision of accurately predicting high credit risk, but shows the greatest ability of all the models used with a score of **9%**.
- This model has the greatest recall scores with a score of **92%** for high credit risk and **94%** for low credit risk.
    - ![EEC Classification Report](https://github.com/JorMerr/Credit_Risk_Analysis/blob/main/img/class_rep_eec.JPG)

## Summary
Overall, analysis shows that the most suitable type of machine learning model to predict high credit risk with our dataset are the ensemble models, BalancedRandomForestClassifier and EasyEnsembleClassifier. This analysis indicates that EasyEnsembleClassifier in particular is the most suitable model to apply to the task of determining high credit risk as it has the lowest instance of False Positive predictions with a strong ability to accurately predict low credit risk.