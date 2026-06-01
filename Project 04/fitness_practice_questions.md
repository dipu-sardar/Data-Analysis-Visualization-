# Data Science Foundational Practice: Smart Watch Fitness Tracker Analysis

This practice package is designed to solidify your foundational knowledge of Python, NumPy, Pandas, Matplotlib, and Seaborn. You will be working with a realistic dataset generated from smart fitness wearables tracking daily user metrics.

---

## The Dataset Description
The accompanying dataset `fitness_tracker_logs.csv` contains daily activity records from three distinct wearable devices (`WD-01`, `WD-02`, `WD-03`). The tracking period covers a sequence of days in May 2026.

### Columns:
- **Date**: The recording date (YYYY-MM-DD).
- **Device_ID**: Unique identifier for the smart wearable device.
- **Steps**: Total steps walked during the day (contains missing entries).
- **Active_Minutes**: Total duration of moderate-to-vigorous physical activity in minutes.
- **Calories_Burned**: Estimated total energy expenditure in kilocalories.
- **Sleep_Quality**: Categorical rating of the user's sleep (`Excellent`, `Good`, `Fair`, `Poor`; contains missing entries).
- **Avg_Heart_Rate**: The average heart rate recorded in beats per minute (BPM; contains missing entries).

---

## Practice Questions

### Section 1: Data Loading & Exploration
1. **Question 1**: Load the `fitness_tracker_logs.csv` file into a Pandas DataFrame named `df`. Display the dimensions (shape) of the dataset and print the data types of all columns.
2. **Question 2**: Inspect the first 5 rows of the DataFrame. Write a snippet to calculate and display the exact number of missing (null) values present in each column.

### Section 2: Data Cleaning & Manipulation
3. **Question 3**: Clean the dataset by handling missing values. Impute the null values in the `Steps` column with the median value of that column. For the `Sleep_Quality` column, fill the missing values with the string `'Unknown'`. Save these updates into the DataFrame.
4. **Question 4**: Create a new engineered feature column named `Calories_Per_Active_Minute`. This should represent the ratio of `Calories_Burned` to `Active_Minutes` for each row.
5. **Question 5**: Filter the DataFrame to extract rows where the user walked more than `10,000` steps **and** achieved a `Sleep_Quality` rating of either `'Good'` or `'Excellent'`.
6. **Question 6**: Sort the entire DataFrame based on the `Calories_Burned` column in descending order, and reset the row index without keeping the old index.

### Section 3: Mathematical & Statistical Analysis
7. **Question 7**: Use NumPy or Pandas to compute the fundamental statistical summary of the `Avg_Heart_Rate` column. Specifically, find its mean, median, variance, and standard deviation (ensure handling or omitting any remaining missing values properly).
8. **Question 8**: Perform an aggregation operation: Group the dataset by `Device_ID` and calculate both the **total** steps taken and the **average** active minutes for each device.

### Section 4: Data Visualization
9. **Question 9**: Using Matplotlib or Seaborn, construct a bar plot showing the total `Steps` accumulated by each `Device_ID`. Add a clear title, axis labels, and color accents.
10. **Question 10**: Create a scatter plot using Seaborn to examine the relationship between `Active_Minutes` (independent variable on the X-axis) and `Calories_Burned` (dependent variable on the Y-axis). Color the data points by their respective `Device_ID` and add a title and grid lines to make the chart ready for a data report.
