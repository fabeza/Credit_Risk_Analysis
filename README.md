# Credit Risk Analysis

## Overview
The purpose of this analysis is determining which machine learning model is better at predicting credit risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different imbalance correction techniques were used to train the models: over-sampling methods (RandomOverSampler and SMOTE), under-sampling methods (ClusterCentroids), a combination of over- and under-sampling methods (SMOTEENN), and emsemble methods (BalancedRandomForestClassifier and EasyEnsembleClassifier). Subsequently, each model's performance was evaluated by calculating their accuracy score and generating a confusion matrix and imbalanced classification report.

Dataset: [LoanStats_2019Q1](https://github.com/fabeza/Credit_Risk_Analysis/blob/6289fe6ce8ac35c3e425c840b8a44a820867e194/Resources/LoanStats_2019Q1.csv)

## Results

* **RandomOverSampler**

![RandomOverSampler.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/d8712114a75309025fb6f229efb2e0d216a37fe4/Resources/RandomOversampler.png)

    1. The RandomOverSampler model had an accuracy score of 0.65, which means 65% of the model's predictions were correct. 
    2. This model returned a precision score of 0.01 and a recall score of 0.71 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.60.

* **SMOTE**

![SMOTE.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/d8712114a75309025fb6f229efb2e0d216a37fe4/Resources/SMOTE.png)

    1. The SMOTE model also had an accuracy score of 0.65, which means 65% of the model's predictions were correct. 
    2. This model returned a precision score of 0.01 and a recall score of 0.63 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.68.

**ClusterCentroids**

![ClusterCentroids.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/d8712114a75309025fb6f229efb2e0d216a37fe4/Resources/ClusterCentroids.png)

    1. The ClusterCentroids model had an accuracy score of 0.54, which means 54% of the model's predictions were correct. 
    2. This model returned a precision score of 0.01 and a recall score of 0.69 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.40.

**SMOTEEN**

![SMOTEENN.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/4ea625bf7773f0c5cd8cc30a32149cae63ca18f1/Resources/SMOTEENN.png)

    1. The SMOTEENN model had an accuracy score of 0.64, which means 64% of the model's predictions were correct. 
    2. This model returned a precision score of 0.01 and a recall score of 0.72 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.57.

**BalancedRandomForestClassifier**

![BalancedRandomForestClassifier.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/d8712114a75309025fb6f229efb2e0d216a37fe4/Resources/BalancedRandomForestClassifier.png)

    1. The BalancedRandomForestClassifier model had an accuracy score of 0.88, which means 88% of the model's predictions were correct. 
    2. This model returned a precision score of 0.03 and a recall score of 0.67 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.89.

**EasyEnsembleClassifier**

![EasyEnsembleClassifier.png](https://github.com/fabeza/Credit_Risk_Analysis/blob/d8712114a75309025fb6f229efb2e0d216a37fe4/Resources/EasyEnsembleClassifier.png)

    1. The EasyEnsembleClassifier model had an accuracy score of 0.94, which means 94% of the model's predictions were correct. 
    2. This model returned a precision score of 0.09 and a recall score of 0.92 for the high risk loans.
    3. The precision and recall scores for the low risk loans were 1 and 0.94.

## Summary

The table below helps visualize a summary of the performance of each applied model. They're ordered left to right by recall score, which represents the model's ability to correctly predict high risk loans.

| Score/Model | EasyEnsembleClassifer | BalancedRandomForestClassifer | SMOTE | SMOTEENN | RandomOverSampler | ClusterCentroids |
| --- | --- | --- | --- | --- | --- | --- |
| Accuracy | 0.94 | 0.88 | 0.65 | 0.64 | 0.65 | 0.54 |
| Precision | 0.99 | 0.99 | 0.99 | 0.99 | 0.99 | 0.99 |
| Recall | 0.94 | 0.89 | 0.68 | 0.57 | 0.61 | 0.40 |

The EasyEnsembleClassifier is the model that returned the best results out of the six models applied to the credit risk dataset. Its highest accuracy score means 94% of its predictions were correct, and the higher precision and recall scores mean it did better than the other models when predicting high/low risk loans correctly.


