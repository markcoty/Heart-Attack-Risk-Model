## Heart Attack Prediction Model

1. Project Objective:
To develop a predictive model using logistic regression and other machine learning techniques to determine the likelihood of patients experiencing a heart attack, based on clinical and diagnostic data.

2. Data Collection and Cleaning
Objective: Obtain, clean, and understand the dataset to prepare it for analysis and modeling.

  - 2.1 Dataset Information
    - Dataset Name: Heart Attack Analysis & Prediction Dataset
    - Source: [Dataset Link](https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset)
    - Shape of Data: 303×14

  - 2.2 Data Cleaning
    - No missing values were found.
    - Renamed columns for clarity.
    - Target Variable: Risk Level (0: Less Risk, 1: High Risk)

  - 2.3 Feature Classification
    - The categorical columns are: 'sex', 'exercise_induced_angina', 'num_major_vessels', 'chest_pain_type', 'fasting_blood_sugar', 'resting_ecg', 'slope', 'thal_rate'
    - The continuous columns are: 'age', 'resting_bp', 'cholesterol', 'max_heart_rate', 'previous_peak'
    - The target column is: ‘risk_level’

  - 2.4 Descriptive Statistics: **See "Exploratory Data Analysis" folder for details.**
    - Summary statistics for continuous features.
    - Unique value counts for categorical features.
    - Count plots and violin plots for feature distributions.

3. Exploratory Data Analysis (EDA)

  - 3.1 Key Observations from EDA
    - Gender distribution: Twice as many males as females.
  - Strong associations:
    - Chest Pain Type: Typical angina strongly associated with low risk.
    - Num of Major Vessels: Higher numbers correlated with higher risk.
    - Thalium Stress Test: High scores associated with high risk.
  - Continuous Feature Insights:
    - Age: Most patients are between 40-65.
    - Max Heart Rate: Higher median for high-risk patients.

  - 3.2 Correlation Analysis: **See "Feature Relationships" folder for details.**
    - Heatmaps showed significant correlations between:
      - Previous Peak and Risk Level
      - Number of Major Vessels and Risk Level

4. Model Development
Objective: Build and evaluate logistic regression and alternative models for predicting Risk Level.

  - 4.1 Feature Engineering
    - Encoded categorical variables using one-hot encoding.
    - Normalized continuous variables for consistent scaling.

  - 4.2 Model Selection
    - Logistic Regression (baseline model).
    - Random Forest Classifier.
    - Gradient Boosted Trees (XGBoost).

  - 4.3 Performance Metrics: **See "Predictive Models" folder for details.**
    - Accuracy, Precision, Recall, F1 Score, and AUC-ROC curve.

5. Results: **See "Results" folder for details.**

6. Model Interpretability
  - 6.1 Feature Importance: Top features contributing to predictions:
    - Previous Peak
    - Num Major Vessels
    - Chest Pain Type
    - Thalium Stress Test

  - 6.2 SHAP Analysis
      - Provided insights into how each feature impacted predictions at the individual and population levels.

7. Conclusion and Recommendations

  - 7.1 Key Findings
    - The Gradient Boosted Trees model performed the best, achieving 88% accuracy.
    - Previous Peak and Num Major Vessels were the most significant predictors of heart attack risk.
    - Both continuous and categorical features played critical roles in prediction.

  - 7.2 Practical Implications
    - Physicians and healthcare providers can use this model to identify high-risk patients and prioritize preventative interventions.

  - 7.3 Limitations
    - Dataset size (n=303n = 303n=303) limits generalizability.
    - Further validation needed on diverse populations.

  - 7.4 Future Work
    - Collect more extensive and diverse datasets.
    - Explore ensemble models for improved performance.

All code for this project is available in the: [Notebooks Folder](https://github.com/markcoty/Heart-Attack-Prediction-Model/tree/main/Notebooks)




