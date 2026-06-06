# Data Science Fundamentals: Smart Home Sensor Analysis Practice

This beginner-friendly assignment targets fundamental competencies in data discovery, validation, cleansing, deterministic metrics computation, and relational visualizations using **Python**, **NumPy**, **Pandas**, **Matplotlib**, and **Seaborn**.

---

## Section 1: Data Loading & Exploration

### Question 1
Load the dataset `smart_home_sensor_data.csv` using Pandas. Programmatically inspect its metadata by executing commands to display:
* The first 5 structural rows of the dataset.
* The dimensional shape (rows and columns count).
* The data types of all individual columns alongside their memory usage profiles.

### Question 2
Determine the integrity of the collected dataset:
* Identify which columns contain missing (`NaN`/`Null`) parameters.
* Calculate the exact count of missing entries for each column.
* Deduce the data type of the `Timestamp` column. Is it optimized for time-series extraction tasks?

---

## Section 2: Data Cleaning & Manipulation

### Question 3
Address the missing historical logs discovered within the numeric indices:
* Impute (fill) the missing values in `Temperature_C` using the dataset's global median temperature.
* Impute the missing values in `Humidity_Pct` using the dataset's global mean humidity.
* Drop any rows where the structural status string parameter `Device_Status` is missing. Validate your modifications by checking the new shape of your DataFrame.

### Question 4
Convert data values to clear analytical categories:
* Convert the `Timestamp` column from a standard text string to a true Pandas `datetime64` object.
* Cast the categorical object columns (`Room_Type`, `Motion_Detected`, `Device_Status`) into the memory-optimized `category` data type to demonstrate industrial memory-management techniques.

### Question 5
Filter out specific target records for operational diagnostics:
* Isolate all observation rows where the `Room_Type` matches `'Server Closet'` **and** the recorded `Temperature_C` exceeds `25.0°C`.
* Sort the resulting subset in descending order based on their `Power_Consumption_kWh` values to pinpoint periods of peak load.

---

## Section 3: Mathematical & Statistical Analysis

### Question 6
Leverage NumPy or vector-based Pandas operations to run descriptive environmental audits:
* Compute the global maximum, minimum, and variance values for the `Temperature_C` metrics across the entire home.
* Calculate the standard deviation and the 75th percentile (3rd quartile) value for `Power_Consumption_kWh`.

### Question 7
Execute categorical data segmentation metrics using aggregation principles:
* Group the dataset by `Room_Type` and isolate the `Power_Consumption_kWh` column.
* Apply aggregations to display the aggregate total (`sum`) and the relative metric center (`mean`) for each distinct room type. Which room consumes the highest total energy?

### Question 8
Extract conditional event frequencies:
* Track human presence metrics by evaluating the cross-tabulation or distribution counts of the boolean indicator `Motion_Detected` against specific `Room_Type` domains.
* Determine what percentage of the logs recorded actual physical motion (`'Yes'`).

---

## Section 4: Data Visualization

### Question 9
Analyze continuous single-variable distributions to study environment variation:
* Generate a distribution plot (a combined Histogram and Kernel Density Estimate curve using Seaborn's `sns.histplot(..., kde=True)`) tracking `Temperature_C`.
* Provide descriptive chart layout features including: a custom plot title, explicit X/Y axis labels, and a distinct aesthetic theme (e.g., `sns.set_theme(style='whitegrid')`).

### Question 10
Explore multi-variable trends and operational dependencies:
* Construct a scatter plot using Matplotlib or Seaborn plotting `Temperature_C` on the X-axis against `Power_Consumption_kWh` on the Y-axis.
* Dynamically color-code individual data points using the `hue` variable parameter mapped to `Device_Status` to evaluate if offline units correspond to low sensor footprints.