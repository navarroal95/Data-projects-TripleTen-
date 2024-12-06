# **Zuber Ride-Sharing Analysis for Chicago**

## **Introduction**
Zuber, a new ride-sharing company in Chicago, aims to optimize its services by analyzing passenger preferences, taxi activity across neighborhoods, and the impact of weather on ride patterns. This project focuses on:
1. Understanding the demand for taxi services across different companies and neighborhoods.
2. Analyzing drop-off patterns in Chicago's busiest areas.
3. Testing the hypothesis regarding the influence of weather on ride durations, specifically for rides from the Loop to O'Hare International Airport on Saturdays.

Through exploratory data analysis (EDA) and hypothesis testing, we provide actionable insights to help Zuber enhance its operations and customer satisfaction.

---

## **Project Goals**
- **Identify Demand**: Analyze the number of rides per taxi company and drop-off patterns in Chicago neighborhoods.
- **Evaluate Impact of Weather**: Test whether weather conditions significantly affect ride durations on Saturdays for trips from the Loop to O’Hare International Airport.
- **Insights for Optimization**: Provide recommendations to optimize Zuber’s services.

---

## **Table of Contents**
1. [Introduction](#introduction)
2. [Project Goals](#project-goals)
3. [Tools and Libraries](#tools-and-libraries)
4. [Workflow and Methodologies](#workflow-and-methodologies)
    - [1. Data Loading and Cleaning](#1-data-loading-and-cleaning)
    - [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
    - [3. Hypothesis Testing](#3-hypothesis-testing)
5. [Results](#results)
6. [Conclusions and Key Insights](#conclusions-and-key-insights)
7. [Future Improvements](#future-improvements)
8. [How to Run](#how-to-run)
9. [Contact](#contact)

---

## **Tools and Libraries**
- **Programming Language**: Python
- **Libraries**:
  - **Data Handling**: pandas
  - **Visualization**: matplotlib, seaborn
  - **Statistical Analysis**: scipy (t-test)

---

## **Workflow and Methodologies**

### **1. Data Loading and Cleaning**
Three datasets were analyzed:
1. **Taxi Companies Data**:
   - Columns: `company_name`, `trips_amount`.
   - Represents the number of rides by different taxi companies on November 15-16, 2017.
   - Data Cleaning: No missing values or duplicates were found.

2. **Neighborhood Drop-offs Data**:
   - Columns: `dropoff_location_name`, `average_trips`.
   - Represents average drop-offs in Chicago neighborhoods for November 2017.
   - Data Cleaning: No missing values or duplicates were found.

3. **Rides and Weather Data**:
   - Columns: `start_ts`, `weather_conditions`, `duration_seconds`.
   - Represents ride start times, weather conditions, and ride durations for rides from the Loop to O'Hare International Airport in November 2017.
   - Data Cleaning: Removed 197 duplicate rows, leaving 871 unique entries.

### **2. Exploratory Data Analysis (EDA)**
#### **Taxi Companies Analysis**
- Flash Cab had the highest number of rides (**19,558**), followed by Taxi Affiliation Services and Medallion Leasing.
- A horizontal bar chart revealed a sharp drop-off in ride numbers after the top companies, indicating market dominance by a few players.

#### **Neighborhood Drop-offs**
- The Loop had the highest average drop-offs (**10,727**), followed by River North and Streeterville.
- Drop-offs were concentrated in central business districts and tourist areas, reflecting high demand for taxi services in these neighborhoods.

#### **Top Neighborhoods by Drop-offs**
- A bar chart highlighted the top 10 neighborhoods with the highest average drop-offs in November 2017.

### **3. Hypothesis Testing**
#### **Objective**:
Test whether ride durations from the Loop to O’Hare International Airport differ significantly on rainy Saturdays compared to non-rainy Saturdays.

#### **Hypotheses**:
- **Null Hypothesis (H₀)**: The average ride duration on rainy Saturdays is equal to the average ride duration on non-rainy Saturdays.
- **Alternative Hypothesis (H₁)**: The average ride duration on rainy Saturdays is different from the average ride duration on non-rainy Saturdays.

#### **Statistical Test**:
- An independent samples t-test was conducted.
- **Significance Level (α)**: 0.05.

#### **Results**:
- **T-statistic**: 5.53
- **P-value**: 9.13 × 10⁻⁸ (much lower than 0.05).
- **Conclusion**: We rejected the null hypothesis, concluding that ride durations on rainy Saturdays are significantly different from non-rainy Saturdays.

---

## **Results**

### **Key Findings**
1. **Taxi Company Insights**:
   - Flash Cab is the leading provider, suggesting high customer preference or operational efficiency.
   - The market is dominated by a few key players, with smaller companies having much fewer rides.

2. **Neighborhood Demand**:
   - The Loop, River North, and Streeterville emerged as top neighborhoods for taxi drop-offs, indicating high demand in central and tourist-heavy areas.

3. **Impact of Weather**:
   - Ride durations from the Loop to O’Hare International Airport are significantly longer on rainy Saturdays, showing the influence of weather conditions on travel times.

---

## **Conclusions and Key Insights**

1. **Central District Dominance**:
   - Central business districts like the Loop and River North drive the highest taxi demand. Expanding operations in these areas can maximize revenue for Zuber.

2. **Weather’s Impact**:
   - Rain significantly increases ride durations, particularly on Saturdays. Zuber could factor this into pricing models or ETA estimates to improve customer experience.

3. **Company Competition**:
   - A few key players dominate the taxi market. Zuber should analyze the strategies of these competitors to capture market share effectively.

---

## **Future Improvements**
1. **Expanded Dataset**:
   - Analyze data from additional months to identify seasonal trends.
2. **Granular Weather Analysis**:
   - Explore specific weather variables (e.g., rainfall intensity, temperature) for deeper insights.
3. **Real-Time Predictions**:
   - Develop predictive models for ride durations and demand patterns using machine learning.
4. **Customer Insights**:
   - Analyze customer feedback to identify pain points and improve services.

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/Zuber-Ride-Analysis

