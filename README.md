# COVID-19 Infant Development Analysis

##  Project Overview
This research project analyzes the impact of COVID-19 on infant development by examining growth metrics, speech scores, and milestone achievements. The study uses machine learning models to predict whether infants were affected by COVID-19 based on their developmental data.

##  Dataset Information
- **Source**: Stimulated dataset created from research papers
- **Size**: 12,000 infant records
- **Region**: South India
- **Time Periods**: Pre-COVID, During-COVID, Post-COVID

### Features Included:
1. **Infant_ID** - Unique identifier for each infant
2. **Region** - Geographic region (South India only)
3. **Age_Months** - Infant age in months (0-12 months)
4. **Height_cm** - Infant height in centimeters
5. **Weight_kg** - Infant weight in kilograms
6. **Speech_Score** - Speech development score (30.1-100.0)
7. **Milestone_Score** - Developmental milestone score (18.9-100.0)
8. **Period** - Time period relative to COVID-19
9. **Affected_By_COVID** - Target variable (Yes/No)

##  Research Methodology

### Data Processing Steps:
1. **Data Collection & Loading** - Imported the dataset from CSV
2. **Shuffling & Index Reset** - Randomized data order for unbiased analysis
3. **Feature Selection** - Removed irrelevant columns (Infant_ID, Region, Period)
4. **Missing Value Handling** - Checked and encoded missing values
5. **Feature Scaling** - Standardized numerical features
6. **Label Encoding** - Converted categorical target to numerical
7. **Train-Test Split** - 80-20 split with stratification

### Machine Learning Models Implemented:
1. **XGBoost Classifier** (v2.0) - 99.42% accuracy
2. **HistGradientBoosting Classifier** (Scikit-learn) - 99.54% accuracy
3. **MLP Classifier** (Deep Learning) - 98.92% accuracy
4. **TabPFN Classifier** (Transformer-based) - Attempted but required authentication

### Model Performance:
- **Best Model**: HistGradientBoosting with 99.54% accuracy
- **Confusion Matrix**: Minimal false positives/negatives
- **Classification Report**: High precision and recall for both classes

##  Key Findings

### Feature Importance (XGBoost):
The most important features for predicting COVID-19 impact were:
1. **Milestone_Score** - Highest importance
2. **Weight_kg**
3. **Height_cm**
4. **Age_Months**
5. **Speech_Score**

### Model Comparison:
- **HistGradientBoosting**: Fastest training (1.71 seconds) with highest accuracy
- **XGBoost**: Slightly lower accuracy but excellent performance
- **MLP**: Good accuracy but slower training (5.33 seconds)

##  Technical Implementation

### Libraries Used:
- **Core**: NumPy, Pandas
- **Visualization**: Matplotlib
- **ML Models**: Scikit-learn, XGBoost, TabPFN
- **Preprocessing**: StandardScaler, LabelEncoder

### Code Structure:
1. **Data Preparation** (Steps 1-9)
2. **Model Training & Evaluation** (Step 10)
3. **Feature Importance Visualization** (Step 11)
4. **Future Predictions** (Step 12)

##  How to Run

### Prerequisites:
```bash
pip install numpy pandas scikit-learn xgboost matplotlib
pip install tabpfn  # Note: Requires HuggingFace authentication
```

### Execution:
1. Ensure `updated_infant_dataset.csv` is in the working directory
2. Run the Jupyter notebook cells sequentially
3. Models will train and display performance metrics automatically

##  Research Contribution
This project contributes to understanding COVID-19's impact on early childhood development by:
1. Creating a comprehensive synthetic dataset based on research papers
2. Applying multiple advanced ML models for prediction
3. Identifying key developmental indicators affected by the pandemic
4. Providing a framework for future longitudinal studies

##  Publication
The analysis methods and findings are documented in a research paper submitted for academic publication, focusing on:
- Methodology for creating stimulated infant datasets
- Comparative analysis of ML models for medical prediction
- Insights into pandemic effects on developmental milestones

##  Limitations & Future Work

### Current Limitations:
- Dataset is simulated rather than real-world
- Single geographic region (South India)
- Limited to infants aged 0-12 months
- TabPFN model requires authentication for full access

### Future Enhancements:
1. **Real Data Collection** - Partner with healthcare institutions
2. **Longitudinal Study** - Track infants over longer periods
3. **Geographic Expansion** - Include multiple regions/countries
4. **Additional Features** - Incorporate parental, environmental factors
5. **Deployment** - Develop web application for healthcare professionals

