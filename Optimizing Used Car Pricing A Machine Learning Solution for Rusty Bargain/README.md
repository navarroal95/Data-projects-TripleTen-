# **Optimizing Used Car Pricing: A Machine Learning Solution for Rusty Bargain**

## **Introduction**
In today’s competitive used car market, accurate pricing is critical for attracting buyers while ensuring fair value for sellers. Rusty Bargain, a used car sales service, is developing an app to predict the market value of vehicles based on historical data, enabling users to quickly assess their car's worth. This project involves building and evaluating machine learning models to predict car prices using technical specifications and attributes. By comparing multiple models, this analysis identifies the best approach in terms of prediction accuracy, training speed, and computational efficiency. The insights gained will help Rusty Bargain deploy an efficient pricing tool, enhancing user experience and streamlining operations.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Tools and Libraries](#tools-and-libraries)
- [Steps and Methodologies](#steps-and-methodologies)
  - [1. Data Exploration and Cleaning](#1-data-exploration-and-cleaning)
  - [2. Feature Engineering and Preparation](#2-feature-engineering-and-preparation)
  - [3. Model Training and Evaluation](#3-model-training-and-evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Recommendations](#future-recommendations)
- [How to Run](#how-to-run)
- [Contact](#contact)

---

## **Tools and Libraries**
- **Programming Language**: Python
- **Libraries**:
  - pandas and numpy for data manipulation
  - sklearn for machine learning and evaluation
  - matplotlib and seaborn for visualizations
  - LightGBM for gradient boosting models

---

## **Steps and Methodologies**

### **1. Data Exploration and Cleaning**
- **Objective**: Understand the dataset structure and prepare it for modeling.
- **Key Steps**:
  - Inspected for missing values, duplicates, and outliers.
  - Addressed missing values:
    - Replaced missing categorical values (e.g., `VehicleType`, `FuelType`) with "Unknown."
    - Replaced zeros in the `Power` column with the median.
  - Removed duplicate rows to ensure data quality.
  - Validated dataset readiness for further analysis.

---

### **2. Feature Engineering and Preparation**
- **Steps**:
  - Selected relevant features, excluding non-informative or redundant columns (e.g., `DateCrawled`, `LastSeen`).
  - Applied one-hot encoding for categorical features.
  - Scaled numerical features where necessary.
  - Split the data into training (70%) and testing (30%) sets for model development and evaluation.

---

### **3. Model Training and Evaluation**
- **Models Used**:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
  - LightGBM Regressor
- **Evaluation Metrics**:
  - RMSE (Root Mean Squared Error): Measures prediction accuracy.
  - Training Time: Assesses computational efficiency during model training.
  - Prediction Time: Evaluates the speed of predictions.

---

## **Results**
| **Model**             | **RMSE**  | **Training Time (s)** | **Prediction Time (s)** |
|------------------------|-----------|------------------------|--------------------------|
| Linear Regression      | 3349.52   | 1.31                   | 0.09                    |
| Decision Tree          | 2272.99   | 1.83                   | 0.06                    |
| Random Forest          | 1794.22   | 109.57                 | 3.93                    |
| LightGBM               | 1882.59   | 2.72                   | 0.60                    |

- **Best Model**: Random Forest achieved the lowest RMSE (1794.22), indicating the highest prediction accuracy.
- **Efficiency Trade-off**: LightGBM offered a balance between accuracy and speed, making it a strong alternative.

---

## **Conclusion**
This project successfully developed and evaluated machine learning models for predicting car prices using Rusty Bargain’s historical data. The Random Forest model demonstrated the highest accuracy, while the LightGBM model offered a competitive balance between accuracy and computational efficiency. These findings provide Rusty Bargain with a robust foundation for implementing a pricing tool that delivers accurate, user-friendly price evaluations.

---

## **Future Recommendations**
- **Real-Time Pricing**: Optimize the LightGBM model for deployment in real-time pricing scenarios.
- **Feature Expansion**: Incorporate additional features like market trends or user demographics to improve accuracy.
- **Data Updates**: Continuously update the dataset with new car sales data to enhance model relevance and accuracy.
- **Cross-Platform Integration**: Implement the pricing tool across web and mobile platforms for broader accessibility.

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/Optimizing Used Car Pricing

