# **ICE Video Game Analysis**

## **Introduction**
This project analyzes video game sales data to identify key trends in platform distribution, genre popularity, regional sales performance, and the influence of ESRB ratings. By examining sales data and user/critic ratings, this analysis provides actionable insights for optimizing game development, marketing strategies, and business decisions in the video game industry.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Tools and Libraries](#tools-and-libraries)
- [Steps and Methodologies](#steps-and-methodologies)
  - [1. Data Exploration and Cleaning](#1-data-exploration-and-cleaning)
  - [2. Sales and Platform Analysis](#2-sales-and-platform-analysis)
  - [3. Genre Analysis](#3-genre-analysis)
  - [4. Regional Analysis](#4-regional-analysis)
  - [5. User and Critic Ratings Analysis](#5-user-and-critic-ratings-analysis)
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
  - matplotlib and seaborn for visualizations
  - scipy for statistical analysis
  - Other tools for data exploration and cleaning

---

## **Steps and Methodologies**

### **1. Data Exploration and Cleaning**
- **Objective**: Load and clean the dataset to ensure it is ready for analysis.
- **Key Steps**:
  - Inspected the dataset for missing values and duplicates.
  - Replaced missing `user_score` values labeled "TBD" with `NaN` and converted to numeric.
  - Calculated `total_sales` as the sum of sales across all regions.
  - Dropped rows with missing values for critical columns like `year_of_release`.

---

### **2. Sales and Platform Analysis**
- **Visualizations**:
  - Total game sales by year using bar plots.
  - Total sales by platform over relevant years (2014 onwards).
  - Sales trends for platforms over the years.
- **Key Insights**:
  - PS4 leads in sales during the relevant period, followed by Xbox One and 3DS.
  - Older platforms like PS3 and Xbox 360 showed declining trends, while newer consoles gained traction.

---

### **3. Genre Analysis**
- **Visualizations**:
  - Median sales by genre using bar plots.
- **Key Insights**:
  - Shooter, Sports, and Platform genres had the highest median sales.
  - Role-Playing games dominated in Japan, while Action and Sports were popular in North America and Europe.

---

### **4. Regional Analysis**
- **Regional Insights**:
  - **North America**:
    - Xbox 360 and PS3 led sales, followed by Nintendo Wii.
    - Action and Sports genres dominated the market.
  - **Europe**:
    - PS2 led sales, followed by PS3 and Xbox 360.
    - Action, Shooter, and Racing genres were highly popular.
  - **Japan**:
    - Nintendo DS and PS were top-performing platforms.
    - Role-Playing games had the highest sales, followed by Action and Fighting genres.

---

### **5. User and Critic Ratings Analysis**
- **Key Steps**:
  - Analyzed correlation between critic scores, user scores, and total sales for PS4 games.
  - Performed t-tests to compare user ratings across platforms and genres.
- **Key Insights**:
  - Moderate positive correlation between critic scores and total sales.
  - Negligible correlation between user scores and total sales.
  - Significant differences in user ratings between Xbox One and PC platforms.

---

## **Results**
- **Top Platforms**:
  - PS4, Xbox One, and 3DS dominate sales in recent years.
  - Regional preferences vary, with handheld systems performing strongly in Japan.
- **Top Genres**:
  - Shooter, Sports, and Action are consistently top-selling genres.
  - Role-Playing games are particularly popular in Japan.
- **Critic and User Ratings**:
  - Critic reviews have a moderate impact on sales.
  - User reviews show weaker correlations with sales performance.

---

## **Conclusion**
The analysis provides actionable insights into platform trends, genre preferences, and regional market dynamics. It highlights the importance of targeting specific platforms and genres based on regional preferences and leveraging critic scores to drive sales.

---

## **Future Recommendations**
- **Focus on Leading Platforms**:
  - Prioritize game development for PS4 and Xbox One in North America and Europe.
  - Emphasize handheld systems like Nintendo DS and 3DS in Japan.
- **Target High-Performing Genres**:
  - Invest in Shooter, Sports, and Role-Playing games based on regional demand.
- **Leverage Critic Reviews**:
  - Focus on improving critic scores to enhance game visibility and sales.
- **Tailor Marketing Strategies**:
  - Customize marketing campaigns for each region to align with platform and genre preferences.

---

## **How to Run**
1. Clone this repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/ICE video game analysis

