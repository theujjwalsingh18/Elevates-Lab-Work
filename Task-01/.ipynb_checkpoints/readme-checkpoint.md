# Titanic Dataset - Data Cleaning and Data Preprocessing

## Project Overview

This project involves cleaning and preprocessing the Titanic dataset followed by exploratory data analysis to uncover key insights related to passenger survival. The dataset contains details about Titanic passengers such as age, sex, passenger class, fare, and family information.

---

## Steps Performed

### 1. Importing Libraries

- Pandas, NumPy for data manipulation
- Matplotlib and Seaborn for visualization
- Warnings filter to suppress unnecessary warnings

### 2. Loading Dataset

- Loaded dataset from `Titanic-Dataset.xls`
- Displayed initial records and basic statistics for an overview

### 3. Data Cleaning

- Dropped irrelevant columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Handled missing values:
  - Replaced missing `Age` values with the mean age
  - Dropped rows with missing `Embarked` values
- Verified remaining missing values

### 4. Encoding Categorical Variables

- Converted categorical columns `Sex` and `Embarked` into numeric dummy variables for analysis

### 5. Outlier Detection and Removal

- Visualized outliers using boxplots
- Removed outliers from columns `Age`, `Fare`, `SibSp`, `Parch` using the Interquartile Range (IQR) method

### 6. Exploratory Data Analysis (EDA)

- Visualized survival counts, age distribution, and correlation matrix
- Explored relationships between survival and variables such as gender, passenger class, age, fare, and family size

### 7. Feature Engineering

- Created a new feature `family_size` as the sum of `SibSp` (siblings/spouses aboard) and `Parch` (parents/children aboard)

---

## Key Insights

- Overall survival rate visualized with a bar chart
- Gender differences in survival: females had higher survival rates than males
- Passenger class impacted survival chances: 1st class passengers had better survival
- Age distribution showed survival varied by age groups
- Fare and family size also correlated with survival likelihood

---

## How to Use

1. Clone or download this repository.
2. Make sure you have all required libraries installed (`pandas`, `numpy`, `matplotlib`, `seaborn`).
3. Place the dataset file `Titanic-Dataset.xls` in the same directory as the notebook/script.
4. Run the notebook to reproduce the cleaning, analysis, and visualizations.

---

## Conclusion

This analysis completes the data cleaning and preprocessing of the Titanic dataset and presents meaningful insights through visualizations and statistical summaries. 

Thank you for reviewing this work!

---

## Author

*Ujjwal Kumar Singh*

