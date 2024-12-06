Data-Driven Oil Well Selection: Profitability and Risk Assessment for OilyGiant
Introduction
This project analyzes geological data from three regions to determine the best location for OilyGiant's next oil well development. By leveraging a linear regression model, the project predicts oil reserve volumes and selects the top 200 wells in each region for profitability estimation. The analysis considers key business constraints, such as a $100 million budget and $4.5 thousand revenue per barrel, and uses bootstrapping to assess risk and minimize losses below a 2.5% threshold. Based on the findings, recommendations are made to identify the most profitable and least risky region for development.

Table of Contents
Introduction
Tools and Libraries
Steps and Methodologies
1. Data Exploration and Cleaning
2. Feature Analysis and Visualization
3. Linear Regression Modeling
4. Profit and Risk Assessment
Results
Conclusion
Future Improvements
How to Run
Contact
Tools and Libraries
Programming Language: Python
Libraries:
pandas and numpy for data manipulation
matplotlib and seaborn for data visualization
scikit-learn for machine learning and model evaluation
scipy for statistical bootstrapping
Steps and Methodologies
1. Data Exploration and Cleaning
Objective: Check for missing values, duplicates, and provide an initial overview of the data.
Key Insights:
Data from three regions (Region 0, Region 1, Region 2) contains 100,000 entries each, with no missing values.
Duplicate IDs were identified and removed:
Region 0: 10 duplicates
Region 1: 4 duplicates
Region 2: 4 duplicates
2. Feature Analysis and Visualization
Visualizations:
Histograms: Show frequency distributions of features (f0, f1, f2, and product) for each region.
Box Plots: Highlight outliers and variability in feature values across regions.
Observations:
Region 2 features are more symmetrically distributed, indicating stability.
Regions 0 and 1 exhibit multimodal distributions and more pronounced outliers.
3. Linear Regression Modeling
Goal: Predict oil reserves based on three features (f0, f1, f2).
Process:
Data split into training (75%) and validation (25%) sets.
Features scaled using StandardScaler.
Linear regression model trained and evaluated using RMSE.
Key Results:
Region 0: RMSE = 37.76, Avg Reserves = 92.40 thousand barrels
Region 1: RMSE = 0.89, Avg Reserves = 68.71 thousand barrels
Region 2: RMSE = 40.15, Avg Reserves = 94.77 thousand barrels
4. Profit and Risk Assessment
Profit Calculation:
Top 200 wells with the highest reserves selected in each region.
Region 0 yielded the highest profit: $33.59M.
Bootstrapping:
Simulated profit distributions to assess risk of loss.
Region 1 has the lowest risk (1.5%), followed by Region 0 (6%) and Region 2 (8%).
Break-Even Analysis:
Break-even reserve volume: 111.11 thousand barrels.
All regions fall below this threshold on average.
Results
Profit Analysis:
Region 0: $33.59M
Region 1: $24.15M
Region 2: $25.99M
Risk of Loss:
Region 0: 6%
Region 1: 1.5%
Region 2: 8%
Recommendation: Region 1 is the best choice for oil well development, balancing moderate profit potential with the lowest risk.
Conclusion
The analysis concludes that Region 1 offers the best opportunity for oil well development due to its low risk (1.5%) and moderate profit potential ($24.15M). While none of the regions surpass the break-even threshold on average, Region 1’s stability and profitability make it the most viable option. Future work could focus on cost optimization and advanced predictive modeling to enhance profitability.


