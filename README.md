# Credit_Risk_Analysis
# Credit_Risk_Analysis
## Overview
The purpose of this analysis is to utilize machine learning algorithms to make prediction on credit risk data patterns. For the analysis of the data, supervised machine learning models will be used. Using the credit risk dataset from LendingClub, a peer-to-peer lending services company, I have oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I have used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I have compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. after completing above mentioned tasks, I have evaluated the performance of these models and provided a written recommendation on whether the models should be used to predict credit risk.

## Results
For the analysis, loan_status was considered to be the outcome. Using the count function it was determined that out of all the applications, 68470 applications were low risk and 347 were high risk.
### Balanced Random Forest Classifier



-- The accuracy of the model is 78.78%
-- The high risk precision rate is 4% with recall rate 67%. The F1 score is 7%
-- The low risk precision rate is 100% with recall rate 91%. The F1 score is 95%
### Oversampling



-- The accuracy of the model is 64.13%.
-- The high risk precision rate is 1% with recall rate 60%. The F1 score is 2%. 
-- The low risk precision rate is 100% with recall rate 68%. The F1 score is 81%.
-- The accuracy score is reduced compared to the Balanced Random Forest Classifier. Moreover, there were changes to the high and low risk precision and recall rates as well as the F1 score.
### SMOTE Oversampling



-- The accuracy of the model is 63.74%
-- The high risk precision rate is 1% with recall rate 60%. The F1 score is 2%
-- The low risk precision rate is 100% with recall rate 68%. The F1 score is 81%
-- Use of SMOTE Oversampling didn't make significant changes to the numbers compared to the oversampling. Use of these oversampling methods did not make significant improvements.
### Under Sampling



-- The accuracy of the model is 63.74%
-- The high risk precision rate is 1% with recall rate 60%. The F1 score is 2%
-- The low risk precision rate is 100% with recall rate 68%. The F1 score is 81%
-- The results from undersampling is almost identical to the SMOTE oversampling. There is no improvement in the result.
### Easy Ensemble AdaBoost Classifier



-- The accuracy of the model is 92.54%
-- The high risk precision rate is 7% with recall rate 91%. The F1 score is 14%
-- The low risk precision rate is 100% with recall rate 94%. The F1 score is 97%
-- This algorithm provides the best results compared to other algorithms used in the analysis. 
### Combination (Over and Under) Sampling



-- The accuracy of the model is 63.93%
-- The high risk precision rate is 1% with recall rate 70%. The F1 score is 2%
-- The low risk precision rate is 100% with recall rate 58%. The F1 score is 73%
-- Combination of Over and Under sampling does not improve the results. The results are close to other over and undersampling results. It fails to improve the results by combining the techniques

## Summary
Based on the results of the six models, "Easy Ensemble Adaboost Classifier" provides the best results. The accuracy rate is close to 93% and 7% precision for predicting the high risk applicants with high recall rate. Moreover, the recall rate and F1 for low risk candidate was highest amongst other models. Based on the information, the recommandation is to use "Easy Ensemble Adaboost Classifier" model to perform this type of analysis.

### Summarizing the results based on high risk results
Easy Ensemble AdaBoost Classifier == 92.54% Accuracy, 7% precision, 91% recall and 14% F1 Score
Balanced Random Forest Classifier == 78.78% Accuracy, 4% precision, 67% recall and 7% F1 Score
Oversampling == 64.13% Accuracy, 1% precision, 60% recall and 2% F1 Score
Combination (Over and Under) Sampling == 63.93% Accuracy, 1% precision, 70% recall and 2% F1 Score
Under Sampling == 63.74% Accuracy, 1% precision, 60% recall and 2% F1 Score
SMOTE Oversampling == 63.74% Accuracy, 1% precision, 60% recall and 2% F1 Score
