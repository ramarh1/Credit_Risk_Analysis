# Credit_Risk_Analysis
Module 17 Challenge

## Analysis Overview
For this analyis, we used Python to perform machine learning models to predict credit risks and classify loans requests as bad or good. We oversampled, undersampled, and used a combinatorial approach to analyze the data. We use a handful of alogirthms in this analysis, such as RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier.

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### RandomOverSampler model
<img width="1026" alt="Naive Random Oversampling" src="https://user-images.githubusercontent.com/88624677/147945693-c68b8a83-5e8e-437a-af1d-a2b9bf9a8084.png">

The balanced accuracy score for this model is 66%. Furthermore high_risk precision is 1%, while the sensitivity/recall for high_risk is 61%. The F1 for high_risk loan applicants is only 2%. On the other hand, the precision for low_risk is 100%, the sensitivity/recall is 71%, and the F1 is at 83%, a lot higher than high_risk.

### SMOTE Oversampling model
<img width="1023" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/88624677/147945721-1c2831a0-be56-47e0-9f16-65833733baba.png">

The balanced accuracy score for this model is 63%. The high_precision risk is 1%, sensitivity/recall is 57%, which makes the F1 2%. For the low_risk applicants the precision is 100%, sensitivity/recall at 68%, and the F1 at 81%.

### ClusterCentroids model/Undersampling
<img width="1024" alt="Undersampling" src="https://user-images.githubusercontent.com/88624677/147946077-b416e734-5bd9-4a60-b673-2251db3a4596.png">

The balanced accuracy score for this model is 60%. The high_precision risk is 1%, sensitivity/recall is 61%, which makes the F1 1%. For the low_risk applicants the precision is 100%, sensitivity/recall at 45%, and the F1 at 62%.

### SMOTEENN model
<img width="1017" alt="SMOTEENN Model" src="https://user-images.githubusercontent.com/88624677/147970274-b1636ac4-fd4a-4f6e-a581-215de5e23914.png">

The balanced accuracy score for this model is 64%. The high_precision risk is 1%, sensitivity/recall is 70%, which makes the F1 2%. For the low_risk applicants the precision is 100%, sensitivity/recall at 57%, and the F1 at 73%.

### BalancedRandomForestClassifier model
<img width="1024" alt="BFC Model" src="https://user-images.githubusercontent.com/88624677/147970311-dd10ed1d-84c2-4786-8228-26dd13b284b6.png">

The balanced accuracy score for this model is 90%. The high_precision risk is 3%, sensitivity/recall is 68%, which makes the F1 6%. For the low_risk applicants the precision is 100%, sensitivity/recall at 90%, and the F1 at 95%.

### EasyEnsembleClassifier model
<img width="1069" alt="EEC" src="https://user-images.githubusercontent.com/88624677/147996585-2c1be9f0-81a5-450c-b22f-fb3a01b80306.png">


The balanced accuracy score for this model is 93%. The high_precision risk is 7%, sensitivity/recall is 91%, which makes the F1 14%. For the low_risk applicants the precision is 100%, sensitivity/recall at 94%, and the F1 at 97%.


## Summary

Examining all the machine learning models, we can see that there is overall weak precision for high-risk credit applicants. The model that had the best sensitivity for high-risk credit applicants is the EasyEnsembleClassifier model (EEC model). The EEC model has a recall of 91% for high-risk credit, which means that it detects almost all of high risk credit applicants. However, since the precision is only 7%, there are low-risk credit applicants that are detected falsely as high-risk. Doing so would affect the bank significantly. Since the precision and sensitivity of the models are not at similar percentages for both high-risk and low-risk applicants, it would be wise to not use any of these machine learning models to predict good anad bad applicants.
