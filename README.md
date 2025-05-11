# Microsoft-Classifying-Cybersecurity-Incidents-with-Machine-Learning

This project focuses on building a robust machine learning classification model to predict the triage grade of cybersecurity incidents — True Positive (TP), Benign Positive (BP), or False Positive (FP) — using the comprehensive GUIDE dataset. This work aims to support Security Operation Centers (SOCs) by improving incident triage accuracy and enabling automated threat response.

# 🎯 Problem Statement

As a data scientist at Microsoft, your task is to enhance the efficiency of SOCs by developing a machine learning model capable of accurately classifying cybersecurity incidents. The model should leverage historical evidence and customer responses from the GUIDE dataset to triage incidents into TP, BP, or FP categories. It should also integrate well into real-time guided response systems for enterprise security.


# 💼 Business Use Cases

- Security Operation Centers (SOCs): Streamline triage to prioritize real threats.

- Incident Response Automation: Enable automated actions for faster threat mitigation.

- Threat Intelligence: Improve threat detection using contextual incident history.

- Enterprise Security Management: Minimize false positives, elevate true incident detection.


# 📊 Dataset Overview

The GUIDE dataset includes three hierarchical levels:

- Evidence: Individual items (e.g., IP, email, user data).

- Alert: Aggregated evidences indicating a possible threat.

- Incident: A consolidated record containing multiple alerts.

Size: 1 million triage-annotated incidents with 45 features
Target Classes: TP, BP, FP
Split: 70% Train | 30% Test (stratified by triage grade, OrgId, DetectorId)


# 🔍 Approach

1. Data Understanding & EDA

- Inspected dataset structure, feature types, distributions, and class balance
- Visualized key feature interactions and triage grade distribution

2. Data Preprocessing

- Imputed missing values
- Encoded categorical features (Label Encoding, One-Hot)
- Feature engineering on timestamps and identifiers
- Normalization/standardization applied to numerical features

3. Data Splitting

- Train-validation split (80-20) using stratified sampling on triage grades

4. Model Training & Benchmarking

- Baseline Models: Logistic Regression, Decision Tree
- Advanced Models: Random Forest, XGBoost, LightGBM, Neural Network
- Hyperparameter Tuning: Grid Search, Random Search
- Class Imbalance Handling: SMOTE, Class Weights

5. Model Evaluation

- Metrics: Macro-F1 Score, Precision, Recall
- Cross-validation for stability check

6. Model Interpretation

- Feature importance using SHAP and permutation importance
- Error analysis of misclassified records

7. Final Testing & Deployment Prep

- Evaluated on held-out test set (test.csv)
- Compared performance with baseline

# 📈 Evaluation Metrics

- Macro-F1 Score: Overall performance across TP, BP, FP
- Precision: Relevance of positive predictions
- Recall: Ability to detect true incidents

# 🛠️ Tech Stack & Skills

- Languages: Python
- Libraries: pandas, numpy, scikit-learn, XGBoost, LightGBM, imbalanced-learn, SHAP, matplotlib, seaborn
- Tools: Jupyter, Git, VS Code
- Skills Gained:
      - Data Preprocessing & Feature Engineering
      - ML Model Benchmarking & Evaluation
      - Cybersecurity Contextualization (MITRE ATT&CK)
      - Handling Imbalanced Data
      - Model Interpretability (SHAP, permutation importance)








