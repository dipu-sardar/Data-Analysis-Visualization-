# Hands-On Practice Package: EV Charging Station Analysis

This practice package is designed to reinforce your foundational knowledge of **Python, NumPy, Pandas, Matplotlib, and Seaborn**. You will act as a Data Analyst evaluating performance data from a network of Electric Vehicle (EV) charging stations.

---

## 1. Data Loading & Exploration
### Q1: Initial Inspection
Write a Pandas script to load the `ev_charging_sessions.csv` file. Display its dimensions (total rows and columns) and print the first 5 rows to understand the structure of the data.

### Q2: Schema and Completeness Check
Inspect the data types of each column to ensure they loaded correctly. Write code to count the number of missing (null) values present in each column of the dataset.

---

## 2. Data Cleaning & Manipulation
### Q3: Imputation & Row Deletion
Handle the missing data using the following strategy:
1. Impute (fill) the missing values in the `Charging_Duration_mins` column with the **median** value of that specific column.
2. Permanently drop the rows where `Energy_Consumed_kWh` is missing from the dataset.
Verify that no null values remain after executing your solution.

### Q4: Conditional Subsetting
Filter the cleaned DataFrame to extract rows where the charging session took place at a **'Highway'** station and the user was a **'Subscriber'**. Save this subset as a new variable and display its summary statistics.

### Q5: Feature Engineering & Sorting
Create a new column named `Charging_Speed_kW` which calculates the rate of energy delivery per hour. Use the formula:
$$\text{Charging\_Speed\_kW} = \left(\frac{\text{Energy\_Consumed\_kWh}}{\text{Charging\_Duration\_mins}}\right) \times 60$$
Once the column is created, sort the entire DataFrame by `Charging_Speed_kW` in **descending order** and display the top 5 fastest sessions.

---

## 3. Mathematical & Statistical Analysis
### Q6: Central Tendency and Dispersion
Use NumPy or Pandas functions to compute the **mean**, **median**, and **standard deviation** of the `Cost_USD` column. Round your results to two decimal places.

### Q7: Aggregated Metrics
Group the dataset by `Vehicle_Model`. Calculate the **total energy consumed** (`Energy_Consumed_kWh`) and the **total revenue generated** (`Cost_USD`) for each vehicle model. 

### Q8: Correlation Analysis
Use the appropriate Pandas function to determine the Pearson correlation coefficient between `Battery_Capacity_kWh` and `Energy_Consumed_kWh`. Explain briefly what this coefficient indicates about the relationship between a vehicle's battery capacity and the energy drawn.

---

## 4. Data Visualization
### Q9: Categorical Comparison (Bar Plot)
Using Matplotlib and Seaborn, create a bar plot showing the **average cost** (`Cost_USD`) across the three different `Station_Location` types ('Urban', 'Suburban', 'Highway'). Customize your plot by adding an informative title, distinct axis labels, and a professional, clean color palette (e.g., `'muted'` or `'viridis'`).

### Q10: Bivariate Relationship (Scatter Plot)
Construct a scatter plot using Seaborn to map the relationship between `Charging_Duration_mins` (X-axis) and `Energy_Consumed_kWh` (Y-axis). Use the `hue` parameter to color-code the points based on `User_Type` ('Subscriber' vs. 'Casual'). Add appropriate titles and gridlines to make the chart ready for a business presentation.
