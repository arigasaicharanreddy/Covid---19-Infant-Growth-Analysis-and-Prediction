
**Covid-19 Infant Growth Analysis and Prediction**
---------------------------------------------------------------------------------------
**Project Overview**

This project focuses on building machine learning models to predict infant developmental outcomes based on features such as age, height, weight, speech scores, and period.
It demonstrates an end-to-end ML pipeline, from preprocessing to deployment using Flask + ngrok.

-----------------------------------------------------------------------------------------------------------
**Objectives**

Achieve ~100% validation accuracy on infant development classification

Deploy a Flask web application for real-time predictions

Document the complete ML life-cycle: preprocessing, modeling, optimization, deployment

-------------------------------------------------------------------------------------------------------------
**Dataset**

Source: infant_development_dataset.csv

Split: 75% Training / 25% Testing

Features: Age, Height, Weight, Speech Scores, Milestone Score, Period

Preprocessing:

Missing values → imputed (mean for numeric, mode for categorical)

LabelEncoder → applied for target labels & categorical features

---------------------------------------------------------------------------------------------------------------
**Models Used**

XGBClassifier (~98.7% accuracy)

TabPFNClassifier (~100% accuracy, chosen for deployment)

----------------------------------------------------------------------------------------------------------------

**Model Training & Evaluation**

Trained  XGBClassifier, and TabPFNClassifier

TabPFNClassifier achieved superior accuracy (~100%)

Evaluation Metrics: Accuracy, Confusion Matrix, Classification Report

Balanced precision/recall across all classes


------------------------------------------------------------------------------------------------------------------


**Deployment**

Deployed Flask web application (with ngrok) for real-time predictions

Input: Infant attributes (age, height, weight, speech score, period)

Output: Predicted Development Status → Normal, At-Risk, or Delayed

--------------------------------------------------------------------------------------------------------------------

**Results**

TabPFNClassifier: Accuracy ≈ 100%

XGBClassifier: Accuracy ≈ 98.7%

Example Predictions:

Higher speech score → Normal Development

Below-average growth → At-Risk Development

Delayed speech → Delayed Development

--------------------------------------------------------------------------------------------------------------------------

**Advantages**

Very high accuracy (~100%)

Minimal preprocessing required

Balanced predictions across classes

---------------------------------------------------------------------------------------------------------------------------

**Limitations**

Dataset size is small → limits generalization

Some imbalance in class distribution

Lower interpretability compared to decision trees

-----------------------------------------------------------------------------------------------------------------------------

**Future Scope**

Extend to deep learning models (TabTransformer, BERT for tabular data)

Collect larger datasets for better generalization

Deploy on cloud platforms for healthcare integration

-------------------------------------------------------------------------------------------------------------------------------

**Source Code & Demo**

The full source code (including preprocessing, model training, and Flask app) is included in this repository.

🔗 GitHub: https://github.com/arigasaicharanreddy/Covid---19-Infant-Growth-Analysis-and-Prediction
