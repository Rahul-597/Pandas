# Pandas Functions Summary

This document provides an overview of the Pandas functions used, along with descriptions, the datasets utilized, and installation instructions.

---

## Installation

To use the Pandas library, install it using pip:

```sh
pip install pandas
```

Ensure that you have the necessary dependencies, such as NumPy, installed:

```sh
pip install numpy
```

---

## Datasets Used

The following datasets were used in the scripts:

1. **Salary Data (`Salary_data.csv`)**  
   - Columns: `YearsExperience`, `Salary`  
   - A dataset containing salary details based on years of experience.

2. **Ratings Data (`rating_final.csv`)**  
   - Columns: `userID`, `placeID`, `rating`, `food_rating`, `service_rating`  
   - A dataset representing user ratings of various places.

3. **Sample Data (`sample.csv`)**  
   - Columns: `Roll No.`, `Physics`, `Chemistry`, `Maths`, `Computer`  
   - A dataset containing student scores in various subjects.

---

## Functions Used

### 1. Creating a Pandas Series

```python
import pandas as pd
series = pd.Series([1, 2, 3, 4])
print(series)
```

- Creates a Pandas Series from a list.

---

### 2. Creating an Empty Series

```python
empty = pd.Series([])
print(empty)
```

- Creates an empty Series.

---

### 3. Creating a DataFrame

```python
df = pd.DataFrame()
print(df)
```

- Creates an empty DataFrame.

```python
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
print(df)
```

- Creates a DataFrame from a dictionary.

---

### 4. Reading CSV Files

```python
df = pd.read_csv("Salary_data.csv")
print(df.head())
```

- Reads a CSV file into a Pandas DataFrame.

---

### 5. Checking Data Properties

```python
df.columns
df.shape
df.size
df.info()
df.describe()
```

- Retrieves DataFrame metadata such as column names, shape, size, and summary statistics.

---

### 6. Displaying Specific Rows

```python
df.head()  # First 5 rows
df.tail()  # Last 5 rows
df.head(10)  # First 10 rows
df.tail(-5)  # Drops the last 5 rows
```

- Retrieves specific sections of the dataset.

---

### 7. Handling Missing Values

```python
df.isnull()  # Identifies missing values
df.isnull().sum()  # Counts missing values per column
df.dropna()  # Drops rows with missing values
df.fillna(0)  # Replaces missing values with 0
df.fillna({'Physics': 'none', 'Chemistry': 0, 'Maths': 30})  # Fill specific columns
df.dropna(inplace=True)  # Drops rows with missing values permanently
```

- Provides methods to handle missing values.

---

### 8. Accessing DataFrame Elements

```python
df['column_name']  # Accesses a column
df.iloc[0]  # Accesses the first row
df.iloc[0:3]  # Accesses first three rows
```

- Retrieves specific elements from the DataFrame.

---

### 9. Filtering Data

```python
df[df['YearsExperience'] > 5]
```

- Filters the dataset based on conditions.

---

## Conclusion

This document provides a quick reference for essential Pandas operations used in the scripts. It covers reading CSV files, handling missing data, filtering, and accessing data efficiently.

---
