# **Data-Driven Oil Well Selection: Profitability and Risk Assessment for OilyGiant**

## **Introduction**
This project analyzes geological data from three regions to determine the best location for OilyGiant's next oil well development. By leveraging a linear regression model, the project predicts oil reserve volumes and selects the top 200 wells in each region for profitability estimation. The analysis considers key business constraints, such as a $100 million budget and $4.5 thousand revenue per barrel, and uses bootstrapping to assess risk and minimize losses below a 2.5% threshold.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Tools and Libraries](#tools-and-libraries)
- [Steps and Methodologies](#steps-and-methodologies)
  - [1. Data Exploration and Cleaning](#1-data-exploration-and-cleaning)
  - [2. Feature Analysis and Visualization](#2-feature-analysis-and-visualization)
  - [3. Linear Regression Modeling](#3-linear-regression-modeling)
  - [4. Profit and Risk Assessment](#4-profit-and-risk-assessment)
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
  - matplotlib and seaborn for data visualization
  - scikit-learn for machine learning and model evaluation
  - scipy for statistical bootstrapping

---

## **Steps and Methodologies**

### **1. Data Exploration and Cleaning**
- **Objective**: Check for missing values, duplicates, and provide an initial overview of the data.
- **Key Insights**:
  - Data from three regions (Region 0, Region 1, Region 2) contains 100,000 entries each, with no missing values.
  - Duplicate IDs were identified and removed:  
    - Region 0: 10 duplicates  
    - Region 1: 4 duplicates  
    - Region 2: 4 duplicates  

### **2. Feature Analysis and Visualization**
- **Visualizations**:
  - **Histograms**: Show frequency distributions of features (`f0`, `f1`, `f2`, and `product`) for each region.
  - **Box Plots**: Highlight outliers and variability in feature values across regions.
- **Observations**:
  - Region 2 features are more symmetrically distributed, indicating stability.
  - Regions 0 and 1 exhibit multimodal distributions and more pronounced outliers.

---

## **Results**
- **Profit Analysis**:
  - Region 0: $33.59M  
  - Region 1: $24.15M  
  - Region 2: $25.99M  
- **Risk of Loss**:
  - Region 0: 6%  
  - Region 1: 1.5%  
  - Region 2: 8%  

---

## **Conclusion**
Region 1 is recommended for oil well development based on its combination of low risk (1.5%) and moderate profit ($24.15M).

---

## **Contact**
For any questions or feedback, feel free to reach out:  
- **Email**: navarroal95@gmail.com 
- **LinkedIn**: www.linkedin.com/in/alan-navarro-5a6440232



