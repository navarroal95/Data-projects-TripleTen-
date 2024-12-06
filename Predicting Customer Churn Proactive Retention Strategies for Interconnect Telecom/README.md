# **Predicting Customer Churn for Interconnect: Final Sprint Project**

## **Introduction**
The telecom operator Interconnect aims to proactively reduce customer churn by predicting which clients are at risk of leaving. This project uses machine learning to identify high-risk customers based on their contract, personal, internet, and phone data. By building a robust predictive model, the company can retain clients through targeted offers, personalized plans, and improved service strategies.

---

## **Project Goal**
To develop a machine learning model that predicts customer churn with high accuracy and an optimized AUC-ROC score. The model will help identify churn-prone customers and provide actionable insights to improve retention strategies.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Project Goal](#project-goal)
- [Tools and Libraries](#tools-and-libraries)
- [Steps and Methodologies](#steps-and-methodologies)
  - [1. Data Exploration and Cleaning](#1-data-exploration-and-cleaning)
  - [2. Feature Engineering](#2-feature-engineering)
  - [3. Data Preparation](#3-data-preparation)
  - [4. Model Training and Evaluation](#4-model-training-and-evaluation)
  - [5. Advanced Modeling](#5-advanced-modeling)
  - [6. Feature Importance Analysis](#6-feature-importance-analysis)
  - [7. Model Deployment](#7-model-deployment)
- [Results](#results)
- [Challenges and Solutions](#challenges-and-solutions)
- [Future Improvements](#future-improvements)
- [How to Run](#how-to-run)
- [Contact](#contact)

---

## **Tools and Libraries**
- **Programming Language**: Python
- **Libraries**:
  - pandas, numpy for data manipulation
  - seaborn, matplotlib for visualizations
  - scikit-learn for baseline models and evaluation
  - XGBoost for advanced modeling
  - joblib for model saving and deployment

---

## **Steps and Methodologies**

### **1. Data Exploration and Cleaning**
- **Objective**: Ensure consistency, handle missing values, and detect duplicates.
- **Actions**:
  - Merged contract, personal, internet, and phone datasets using `customerID`.
  - Identified and filled missing service features with "No" for inactive subscriptions.
  - Imputed missing `TotalCharges` values using the median.

---

### **2. Feature Engineering**
- **Goal**: Enhance predictive power by creating meaningful features.
- **Key Features**:
  - **`is_fiber_optic`**: Binary indicator for fiber optic users.
  - **`is_electronic_check`**: Binary indicator for customers using electronic checks.
  - **`has_tech_support`**: Binary indicator for tech support subscribers.
  - **`contract_duration_months`**: Numerical representation of contract type (month-to-month, one year, two years).

---

### **3. Data Preparation**
- Handled class imbalance using manual oversampling.
- Encoded categorical variables using one-hot encoding.
- Scaled numerical features (e.g., `MonthlyCharges`, `tenure`) with `StandardScaler`.

---

### **4. Model Training and Evaluation**
- **Baseline Models**:
  - Logistic Regression: AUC-ROC = 0.848, Accuracy = 81.03%.
  - Decision Tree: AUC-ROC = 0.788, Accuracy = 83.19%.
- **Evaluation Metrics**:
  - Primary: AUC-ROC.
  - Secondary: Accuracy.

---

### **5. Advanced Modeling**
- Trained and evaluated advanced models:
  - Random Forest: AUC-ROC = 0.898, Accuracy = 84.95%.
  - XGBoost: AUC-ROC = 0.943, Accuracy = 90.18%.
- XGBoost emerged as the best model due to its superior predictive performance.

---

### **6. Feature Importance Analysis**
- Used XGBoost to identify influential features:
  - `contract_duration_months`, `is_fiber_optic`, and `has_tech_support` were the most impactful predictors.

---

### **7. Model Deployment**
- Saved the XGBoost model as `best_churn_model.pkl` using joblib for future use and deployment.

---

## **Results**
| **Model**             | **AUC-ROC** | **Accuracy** |
|------------------------|-------------|--------------|
| Logistic Regression    | 0.848       | 81.03%       |
| Decision Tree          | 0.788       | 83.19%       |
| Random Forest          | 0.898       | 84.95%       |
| XGBoost                | 0.943       | 90.18%       |

- **Best Model**: XGBoost, achieving the highest AUC-ROC and accuracy.

---

## **Challenges and Solutions**
1. **Class Imbalance**:
   - Problem: Fewer churned customers in the dataset.
   - Solution: Used manual oversampling to balance the classes.
2. **Missing Values**:
   - Problem: Missing entries in `TotalCharges` and service-related features.
   - Solution: Imputed `TotalCharges` using the median and filled service-related missing values with "No."
3. **Dataset Integration**:
   - Problem: Multiple datasets with partial overlaps.
   - Solution: Merged datasets using `customerID` and validated consistency.

---

## **Future Improvements**
- **Incorporate Customer Feedback**: Include sentiment analysis from customer reviews or complaints to enhance predictions.
- **Precision-Recall Tradeoff**: Optimize thresholds for identifying high-risk customers.
- **Real-Time Updates**: Train models periodically to adapt to evolving customer behavior.
- **Actionable Insights**: Develop strategies based on churn predictions, e.g., targeting high-risk customers with specific offers.

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/Interconnect-Churn-Prediction

