# Data Analysis Practice Problems

This file contains 20 simple problems to practice Python, NumPy, Pandas, Matplotlib, and MySQL using `employee_data.csv`.

---

### Phase 1: Python & NumPy Basics
1. **Read CSV:** Write a Python script to open `employee_data.csv` and print the first 5 rows.
2. **Convert to Array:** Convert the `Salary` column into a NumPy array (skip or remove any empty values).
3. **Salary Raise:** Use the NumPy array to give everyone a 10% raise. Print the original and new salaries.
4. **Basic Statistics:** Find the Mean (average), Median, and Standard Deviation of the `Age` column using NumPy.
5. **Filter Scores:** Use NumPy to find and print all performance scores that are greater than 8.0.

---

### Phase 2: Pandas Data Manipulation
6. **Load & Summary:** Load the CSV file into a Pandas DataFrame. Display `.info()` and `.describe()`.
7. **Fix Missing Values:** Fill the missing value in `Salary` with the median salary. Fill the missing `PerformanceScore` with the mean score.
8. **Filter Rows:** Show rows where the department is "Engineering" and `Remote` is "Yes".
9. **Group By Department:** Group by `Department` and calculate the average salary and average performance score for each.
10. **Find Top Earners:** Find the top 3 highest-paid employees. Sort them from highest to lowest salary.
11. **Date Column:** Convert `JoinDate` to a datetime type. Create a new column named `JoinYear` with just the year.
12. **Count Values:** Count how many employees work remote ("Yes") vs in-office ("No").

---

### Phase 3: Matplotlib Visualization
13. **Age Histogram:** Plot a simple histogram of the `Age` column. Add a title and axis labels.
14. **Department Bar Chart:** Create a bar chart showing the number of employees in each department.
15. **Salary Scatter Plot:** Make a scatter plot with `Age` on the X-axis and `Salary` on the Y-axis.
16. **Salary Pie Chart:** Create a pie chart showing the percentage of total salary spent on each department.

---

### Phase 4: MySQL & Git
17. **Create Table:** Write a SQL query (`CREATE TABLE`) to build a table that matches this CSV file structure.
18. **High Salary Query:** Write a SQL query to select the `Name`, `Department`, and `Salary` of employees earning more than 60,000.
19. **Group By Query:** Write a SQL query to find departments with an average performance score higher than 7.5.
20. **Git Save:** Initialize a Git repository, create a basic `.gitignore` file, and make your first commit with your code.
