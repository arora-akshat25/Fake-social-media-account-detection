Fake Social Media Account Detection using Supervised Machine Learning

This repository contains a machine-learning pipeline developed to detect fake social media accounts using metadata, engagement statistics, and behavioural features. The project evaluates and compares multiple supervised ML algorithms including Logistic Regression, Decision Tree, Random Forest, and XGBoost.

Overview

Fake or automated accounts are a growing issue on modern platforms, often participating in misinformation, spam, and harmful activities. This project implements a supervised classification approach that distinguishes fake from real accounts by analysing profile attributes and user activity behavior.

Dataset and Features

The dataset contains user metadata and behavioural information, including (but not limited to):

Profile verification and confirmation

Subscriber count

Activity metrics (posts, likes, comments, reposts)

Behavioural ratios (posting frequency, content uniqueness)

Metadata presence (photo, mobile, nickname, etc.)

Missing values, inconsistent representations, and text categories were cleaned and transformed into numeric form to enable model training.

Machine Learning Models

The following models were implemented and evaluated:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

XGBoost Classifier

Evaluation metrics include Accuracy, Precision, Recall, F1 score, and Confusion Matrix-based analysis. ROC and AUC curves were also used to compare classifier performance.

Results

Based on test-set performance, the results are:

Model	Accuracy	Precision	Recall	F1
Logistic Regression	94.89%	0.95	0.94	0.95
Decision Tree	96.51%	0.96	0.97	0.97
Random Forest	96.68%	0.96	0.97	0.97
XGBoost	97.19%	0.97	0.97	0.97

(Values taken directly from the experimental analysis)

Models based on ensemble and boosting techniques, particularly Random Forest and XGBoost, showed the strongest performance.

Data Preprocessing

Key preprocessing and feature engineering steps include:

Removal of invalid and irrelevant fields

Handling of binary categorical variables (yes/no type)

Correction of approximately 68,000 missing or inconsistent values

Mean imputation of numeric missing data

Automated numeric conversion across object columns

Complete recovery of previously unusable feature values (full dataset usability after cleaning)

Evaluation

The project includes:

Train-Test split with stratification

Model comparison based on classification metrics

Confusion matrices

ROC-AUC analysis

Feature importance examination

How to Run

Install dependencies:

pip install -r requirements.txt


Open the main notebook:

jupyter notebook poc.ipynb


Run all cells in sequence to reproduce preprocessing, model evaluation, and comparison.

Repository Contents
/poc.ipynb          Main project notebook
/bots_vs_users.csv  Dataset used for training and evaluation
/SMLca.xlsx         Documented research details
/README.md          Project overview


Additional results (plots, evaluation metrics, and images) can be added under a results or images directory.

Conclusion

XGBoost and Random Forest achieved the highest predictive performance, indicating that ensemble learning techniques can reliably detect fake accounts based on behavioural and metadata patterns. The pipeline achieves up to 97.19 percent accuracy and demonstrates strong recall, which is valuable for minimizing false negatives.
