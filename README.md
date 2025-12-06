Fake Social Media Account Detection (Supervised Machine Learning)

A complete supervised machine learning pipeline for detecting fake social media accounts using profile metadata, behavioural patterns, and engagement statistics. The project implements and compares multiple classification models including Logistic Regression, Decision Tree, Random Forest, and XGBoost, achieving up to 97.19 percent accuracy on the evaluation set.

Overview

Fake or automated accounts are increasingly common on modern platforms and often contribute to misinformation, spam, and malicious activity. This project builds a classification-based detection system capable of distinguishing real and fake accounts through metadata signals and user behaviour analytics.

Dataset and Features

The dataset includes user metadata and behavioural fields such as:

Profile verification and confirmation signals

Subscriber and follower statistics

Posting behaviour (frequency, engagement ratios, content patterns)

Activity metrics (likes, reposts, comments, views)

Metadata presence (photo, mobile phone, nickname fields)

All categorical and inconsistent fields were processed into numeric form, and missing values were imputed. Approximately 68,000 unusable values were cleaned, resulting in full dataset usability for downstream modelling.

Machine Learning Models Used

The following models were developed and evaluated:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

XGBoost Classifier

Evaluation metrics include: Accuracy, Precision, Recall, F1 score, Confusion Matrix, ROC and AUC analysis, and feature importance inspection.

Results

Performance based on the test set:

Model	Accuracy	Precision	Recall	F1
Logistic Regression	94.89%	0.95	0.94	0.95
Decision Tree	96.51%	0.96	0.97	0.97
Random Forest	96.68%	0.96	0.97	0.97
XGBoost	97.19%	0.97	0.97	0.97

Ensemble and boosting-based approaches, particularly XGBoost and Random Forest, produced the strongest performance in identifying fake accounts accurately while preserving recall.

Data Preprocessing

Main preprocessing steps include:

Removal of irrelevant and invalid fields

Handling of binary categorical variables

Automated numeric conversion

Mean imputation of numeric missing data

Full recovery of previously unusable feature values

Stratified train-test splitting

Evaluation and Analysis

Methods applied during evaluation:

Model comparison and benchmarking

Confusion matrix visualisation

ROC-AUC analysis

Feature importance ranking

These provide interpretability and allow comparison between different ML methods.

Execute cells sequentially to reproduce preprocessing, training, and evaluation.

Conclusion

XGBoost and Random Forest achieved the highest predictive performance, confirming that non-linear ensemble models offer strong capability in detecting fake social media accounts based on behavioural signals and profile metadata. The pipeline reaches up to 97.19 percent accuracy with high recall, which is particularly important when minimising false negatives.
