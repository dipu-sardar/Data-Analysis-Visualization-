# Data Science Foundational Practice: Wearable Fitness Tracker Analysis

This practice package is designed to test and solidify your foundational skills in **Python, NumPy, Pandas, Matplotlib, and Seaborn**. You will be working with a realistic dataset containing daily monitoring summaries from various wearable fitness trackers.

---

## 1. Data Loading & Exploration

### Question 1
Load the dataset `fitness_tracker_logs.csv` into a Pandas DataFrame. Display the first 8 rows of the dataset, and programmatically print out the total number of rows and columns present in the file.

### Question 2
Inspect the dataset's metadata. Print out the data types of all columns and determine the exact number of missing (null) values inside each column. Which columns contain missing data?

---

## 2. Data Cleaning & Manipulation

### Question 3
Handle the missing values in the dataset using the following specific strategy:
- For the numerical columns `Steps` and `Active_Minutes`, fill the missing values with their respective column **median**.
- For rows where `Sleep_Duration_Hours` or `Weather_Condition` is missing, **drop** those rows completely from the DataFrame.
- Verify that your final clean DataFrame no longer contains any missing values.

### Question 4
Transform the time-series elements:
- Convert the `Date` column from an object/string data type into a proper pandas `datetime` object.
- Create a new column named `Month` that extracts the full month name (e.g., January, February) from the `Date` column.

### Question 5
Filter the dataset to isolate high-performing days:
- Find all log entries where the user achieved more than `10,000` steps AND burned more than `2,500` calories.
- Sort this filtered subset by `Calories_Burned` in descending order, and display the top 5 records.

---

## 3. Mathematical & Statistical Analysis

### Question 6
Use **NumPy** functions on your clean DataFrame to compute the following metrics for the `Heart_Rate_Avg` column:
- Overall arithmetic mean
- Median value
- Standard deviation
- 25th and 75th percentiles

### Question 7
Analyze device performance using aggregations:
- Group the data by `Device_Type`.
- Compute both the **average** `Distance_km` covered and the **total** `Calories_Burned` for each device tracker.
- Rename the aggregated columns to `Average_Distance_km` and `Total_Calories_Burned` respectively.

### Question 8
Explore relationship matrices:
- Compute the Pearson correlation matrix for all numerical variables (`Age`, `Steps`, `Distance_km`, `Calories_Burned`, `Active_Minutes`, `Sleep_Duration_Hours`, `Heart_Rate_Avg`).
- Identify which pair of variables displays the strongest positive correlation.

---

## 4. Data Visualization

### Question 9
Using **Seaborn** and **Matplotlib**, create a clean, professional bar plot that illustrates the average number of `Steps` taken across different `Weather_Condition` categories. 
- Ensure your plot contains descriptive X and Y axis labels, a prominent title, and a cohesive color palette (e.g., `muted` or `viridis`).

### Question 10
Generate a scatter plot using **Matplotlib** or **Seaborn** to map the relationship between `Active_Minutes` (X-axis) and `Calories_Burned` (Y-axis).
- Use the `Gender` column as a color hue (or marker differentiator) to see if patterns vary across genders.
- Add a visible grid and a title to complete your visualization.