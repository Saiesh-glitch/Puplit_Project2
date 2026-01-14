# Puplit_Project2
# 1. Forecasting: Day-Ahead Solar Energy Forecasting using SARIMA
# Problem Understanding
The goal of this project is to forecast daily solar energy one day ahead using historical solar irradiance data. Accurate day-ahead forecasts help in renewable energy planning, grid stability, and efficient solar power utilization.

# Approach & Methodology
Converted raw hourly solar irradiance data into daily solar energy to reduce noise and align with real-world energy planning.
Cleaned missing values (-999) and constructed a proper datetime index.
Performed exploratory data analysis to identify trends and seasonality.
Used a time-aware train–test split (85% train, 15% test).
Built a SARIMA (1,1,1) × (1,1,1,7) model to capture trend and weekly seasonality.
Evaluated performance using MAE, RMSE, and MAPE.

# Results & Accuracy
MAE: ~294 Wh/m²
RMSE: ~341 Wh/m²
MAPE: 8.35%
Forecast Accuracy: ~92%

# Challenges Faced
Handling missing data encoded as -999
Avoiding misleading baseline comparisons due to low test-window variability
Balancing interpolation with realistic evaluation

# Design & Creative Decisions
Chose daily energy forecasting instead of hourly for operational relevance.
Selected SARIMA for interpretability and robustness over complex ML models.
Included confidence intervals to communicate forecast uncertainty.

# Tools & Technologies
Python
pandas, numpy – Data preprocessing
matplotlib – Visualization
statsmodels – SARIMA modeling
scikit-learn – Evaluation metrics


# 2. Classification

# Problem Understanding
The objective of this project is to build a classification model that predicts a customer’s gender based on demographic information. Such classification tasks are commonly used in customer segmentation, targeted marketing, and business analytics.

# Approach & Methodology
Loaded customer demographic data from a CSV file.
Selected Age as the independent feature.
Used Gender as the target variable.
Encoded categorical labels using Label Encoding.
Split the data into training (80%) and testing (20%) sets.
Trained a Random Forest Classifier to learn patterns between age and gender.
Evaluated model performance using accuracy and classification metrics.

# Tools
Python
Libraries:
pandas – Data loading and manipulation
scikit-learn – Model building and evaluation
RandomForestClassifier
Train-test split
Accuracy score
Classification report

# Model Evaluation
Evaluation Metrics Used:
Accuracy
Precision
Recall
F1-score (via classification report)

# Challenges Faced
Limited feature set (only age used for prediction).
Potential class imbalance in gender distribution.
Risk of oversimplification due to minimal input variables.
