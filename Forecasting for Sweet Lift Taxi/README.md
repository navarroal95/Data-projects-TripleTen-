# **Optimizing Peak-Time Driver Availability: Hourly Demand Forecasting for Sweet Lift Taxi**

## **Introduction**
Sweet Lift Taxi aims to enhance driver availability during peak times by accurately forecasting hourly taxi demand using historical airport order data. This project developed a predictive model to estimate hourly taxi orders, enabling better resource allocation and improved service during high-demand periods. 

Key methodologies included time series data processing, feature engineering, and model evaluation across various machine learning algorithms. The project achieved the desired RMSE threshold of 48 using the LightGBM model, providing Sweet Lift Taxi with a reliable tool for operational planning.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Tools and Libraries](#tools-and-libraries)
- [Steps and Methodologies](#steps-and-methodologies)
  - [1. Data Preparation and Exploration](#1-data-preparation-and-exploration)
  - [2. Time Series Analysis](#2-time-series-analysis)
  - [3. Feature Engineering](#3-feature-engineering)
  - [4. Model Training and Evaluation](#4-model-training-and-evaluation)
  - [5. Hyperparameter Tuning](#5-hyperparameter-tuning)
  - [6. Final Testing](#6-final-testing)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Improvements](#future-improvements)
- [How to Run](#how-to-run)
- [Contact](#contact)

---

## **Tools and Libraries**
- **Programming Language**: Python
- **Libraries**:
  - pandas and numpy for data manipulation
  - matplotlib for visualizations
  - scikit-learn for machine learning and model evaluation
  - LightGBM for gradient boosting
  - statsmodels for time series decomposition
  - RandomizedSearchCV for hyperparameter tuning

---

## **Steps and Methodologies**

### **1. Data Preparation and Exploration**
- **Objective**: Load, clean, and explore the dataset to ensure data integrity.
- **Key Insights**:
  - Dataset contains 26,496 rows with no missing or duplicate values.
  - Columns: `datetime` (timestamp) and `num_orders` (number of taxi orders).
  - Cleaned dataset prepared for resampling and feature engineering.

---

### **2. Time Series Analysis**
- **Objective**: Understand demand patterns over time.
- **Visualizations**:
  - **Taxi Orders Over Time**: Identified demand fluctuations and increasing trends.
  - **Seasonal Decomposition**:
    - **Trend**: Showed gradual increase in taxi orders.
    - **Seasonality**: Highlighted repeating daily and weekly patterns.
    - **Residuals**: Captured random fluctuations.
  - **Rolling Mean**: Smoothed short-term noise to highlight overall trends.

---

### **3. Feature Engineering**
- **Features Created**:
  - `hour`: Hour of the day.
  - `day_of_week`: Day of the week.
  - `month`: Month of the year.
- Resampled data by hour, summing `num_orders` to aggregate taxi demand hourly.

---

### **4. Model Training and Evaluation**
- **Objective**: Train and evaluate models to predict hourly demand.
- **Models Tested**:
  - Linear Regression
  - Decision Tree
  - Random Forest
  - Gradient Boosting
  - LightGBM
- **Evaluation Metric**: RMSE (Root Mean Squared Error)
- **Results**:
  - Decision Tree and LightGBM performed best.
  - LightGBM achieved RMSE: 48.31, meeting the target threshold.

---

### **5. Hyperparameter Tuning**
- **Objective**: Optimize LightGBM model using RandomizedSearchCV and TimeSeriesSplit.
- **Best Parameters**:
  - Learning Rate: 0.2
  - Number of Leaves: 31
  - Subsample: 0.6
  - Max Depth: -1 (no limit)
  - n_estimators: 100
- **Cross-validated RMSE**: 27.16

---

### **6. Final Testing**
- **Objective**: Evaluate the tuned model on the test set.
- **Results**:
  - Test RMSE: 22.96 (well below the target threshold of 48).
  - Model successfully meets performance requirements.

---

## **Results**
- **Key Performance Metrics**:
  - Final Model: LightGBM
  - Test RMSE: 22.96
  - Meets target RMSE threshold of 48.

---

## **Conclusion**
This project successfully developed a predictive model for hourly taxi demand, enabling Sweet Lift Taxi to improve driver availability during peak times. The optimized LightGBM model achieved excellent accuracy, surpassing the target RMSE threshold. The project demonstrates the value of data-driven decision-making for operational efficiency in ride-hailing services.

---

## **Future Improvements**
- **Incorporate Additional Features**:
  - Weather data or traffic patterns to enhance predictions.
- **Expand Temporal Coverage**:
  - Use data from other locations for broader applicability.
- **Deploy Model**:
  - Integrate the model into an API for real-time forecasting.

---

## **How to Run**
1. Clone this repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/Forecasting for Sweet Lift Taxi

