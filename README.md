
**Covid-19 Infant Growth Analysis and Prediction**
---------------------------------------------------------------------------------------
**Project Overview**

The COVID-19 pandemic introduced unprecedented changes to social interactions, healthcare access, and daily routines, potentially impacting early childhood development. This project addresses the critical need to understand and classify how different pandemic periods may have influenced infant developmental trajectories. By analyzing comprehensive infant development data, we've built robust machine learning models that can accurately identify the developmental period based on key growth and milestone metrics.

-----------------------------------------------------------------------------------------------------------
**Objectives**

Achieve ~99% accuracy on infant development classification

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

catboostClassifier (~99% accuracy, chosen for deployment)

----------------------------------------------------------------------------------------------------------------

**Model Training & Evaluation**

Trained  XGBClassifier, and catboostClassifier

catboostClassifier achieved superior accuracy (~99%)

Evaluation Metrics: Accuracy, Confusion Matrix, Classification Report

Balanced precision/recall across all classes


------------------------------------------------------------------------------------------------------------------


**Deployment**

Deployed Flask web application (with ngrok) for real-time predictions

Input: Infant attributes (age, height, weight, speech score, period)

Output: Predicted Development Status → Normal, At-Risk, or Delayed

--------------------------------------------------------------------------------------------------------------------

**Results**

catboostClassifier: Accuracy ≈ 99%

XGBClassifier: Accuracy ≈ 98.7%

Example Predictions:

Higher speech score → Normal Development

Below-average growth → At-Risk Development

Delayed speech → Delayed Development

--------------------------------------------------------------------------------------------------------------------------

**Advantages**

Very high accuracy (~99%)

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
