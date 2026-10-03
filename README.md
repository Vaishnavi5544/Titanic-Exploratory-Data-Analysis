# 🚢 Titanic Exploratory Data Analysis

An Exploratory Data Analysis (EDA) project on the Titanic dataset using Python. The project explores passenger survival patterns, data quality issues, distributions, potential outliers, and statistical relationships between variables.

---

## 📌 Project Overview

The Titanic dataset contains information about passengers who travelled on the RMS Titanic. This project uses Python to inspect, clean-check, visualize, and statistically test the data in order to understand which factors were associated with passenger survival.

The analysis covers:

- Passenger survival
- Gender and survival
- Passenger class and survival
- Age distribution
- Fare distribution
- Missing values and duplicate records
- Potential outliers
- Statistical hypothesis testing

The complete analysis is available in the Jupyter Notebook `Titanic_EDA_Analysis.ipynb`.

---

## 🎯 Objectives

- Understand the structure and quality of the Titanic dataset
- Identify missing values and duplicate records
- Analyze overall survival and survival across groups
- Study the distributions of age and fare
- Detect potential outliers in fare using the IQR method
- Test relationships using appropriate statistical tests
- Present findings clearly with visualizations and simple explanations

---

## ❓ Questions Explored

1. What percentage of passengers survived?
2. Did gender have an association with survival?
3. Did passenger class have an association with survival?
4. How was age distributed among passengers?
5. Was there a significant difference in age distributions between survivors and non-survivors?
6. What does the fare distribution look like?
7. Are there potential outliers in passenger fares?
8. What missing values are present in the dataset?
9. Are there duplicate records?

---

## 📊 Dataset Information

The analysis uses the **Titanic dataset**, which contains **891 rows** and **12 columns**.

| Variable | Description |
|---|---|
| PassengerId | Unique passenger identifier |
| Survived | Survival status (0 = No, 1 = Yes) |
| Pclass | Passenger class (1st, 2nd, 3rd) |
| Name | Passenger name |
| Sex | Passenger gender |
| Age | Passenger age |
| SibSp | Number of siblings/spouses aboard |
| Parch | Number of parents/children aboard |
| Ticket | Ticket number |
| Fare | Passenger fare |
| Cabin | Cabin number |
| Embarked | Port of embarkation |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Python** | Core programming language |
| **Pandas** | Data loading, inspection, and manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical visualization |
| **SciPy** | Statistical hypothesis testing |
| **Jupyter Notebook** | Interactive analysis environment |

---

## 🔍 Exploratory Data Analysis

This section presents **descriptive findings**, which summarize what the data shows. Statistical conclusions are covered separately in the next section.

### Analysis Performed

1. Dataset inspection
2. Data types analysis
3. Missing-value analysis
4. Duplicate detection
5. Survival distribution analysis
6. Gender vs survival analysis
7. Passenger class vs survival analysis
8. Age distribution analysis
9. Age vs survival analysis
10. Fare distribution analysis
11. Fare outlier detection using IQR
12. Chi-Square hypothesis testing
13. Mann-Whitney U hypothesis testing
14. Data quality assessment
15. Key findings and conclusions

### Overall Survival

| Outcome | Passengers |
|---|---:|
| Survived | 342 |
| Did not survive | 549 |

The overall survival rate was approximately **38.38%**, meaning most passengers in the dataset did not survive.

### Survival by Gender

| Gender | Approx. Survival Rate |
|---|---:|
| Female | 74.2% |
| Male | 18.9% |

### Survival by Passenger Class

| Passenger Class | Approx. Survival Rate |
|---|---:|
| 1st Class | 63% |
| 2nd Class | 47% |
| 3rd Class | 24% |

### Age Distribution

- Many passengers were between approximately 20 and 35 years old.
- The dataset has **177 missing Age values**, which should be kept in mind when interpreting age-based results.
- A boxplot was used to compare the age distributions of survivors and non-survivors.

### Fare Distribution

The Fare variable is **strongly right-skewed**.

| Statistic | Value |
|---|---:|
| Mean | 32.20 |
| Median | 14.45 |
| Minimum | 0 |
| Maximum | 512.33 |

The mean is much higher than the median, which shows the influence of a smaller number of high fare values.

### Fare Outlier Detection (IQR Method)

| Measure | Value (approx.) |
|---|---:|
| Q1 | 7.91 |
| Q3 | 31.00 |
| IQR | 23.09 |
| Upper outlier boundary | 65.63 |
| Potential outliers | 116 observations |

These values are described as **potential outliers**, not errors. They were not automatically removed because they may represent genuine high-cost tickets or group bookings.

---

## 🧪 Statistical Hypothesis Testing

Statistical tests were used to check whether the patterns seen in the descriptive analysis are unlikely to be due to chance alone. A significance level of **0.05** is used for interpretation.

| Test | Variables | Test Statistic | P-value | Degrees of Freedom | Conclusion |
|---|---|---:|---:|---:|---|
| Chi-Square Test of Independence | Gender vs Survival | 260.717 | 1.197 × 10⁻⁵⁸ | 1 | Statistically significant association |
| Chi-Square Test of Independence | Passenger Class vs Survival | 102.889 | 4.549 × 10⁻²³ | 2 | Statistically significant association |
| Mann-Whitney U Test | Age (Survivors vs Non-survivors) | U = 57,682 | 0.1605 | – | No statistically significant difference found |

### Interpretation

- **Gender and survival:** The p-value is far below 0.05, so there is a statistically significant association between gender and survival in this dataset.
- **Passenger class and survival:** The p-value is far below 0.05, so there is a statistically significant association between passenger class and survival in this dataset.
- **Age and survival:** The p-value (0.1605) is greater than 0.05, so the analysis does **not** provide sufficient statistical evidence of a difference in age distributions between survivors and non-survivors.

> **Note:** A statistically significant association shows that two variables are related in the data. It does not, by itself, prove that one variable caused the other.

---

## 🧹 Data Quality Issues

### Missing Values

| Column | Missing Values | Approx. Percentage |
|---|---:|---:|
| Age | 177 | 19.87% |
| Cabin | 687 | 77.10% |
| Embarked | 2 | 0.22% |

The **Cabin** column has a particularly high percentage of missing values, so it should be used with caution in any further analysis.

### Duplicate Records

No duplicate records were found in the dataset.

---

## 📈 Visualizations

The notebook includes the following visualizations, created using **Matplotlib** and **Seaborn**:

| Visualization | Purpose |
|---|---|
| Survival distribution | Shows the number of survivors and non-survivors |
| Survival rate by gender | Compares survival between male and female passengers |
| Survival rate by passenger class | Compares survival across 1st, 2nd, and 3rd class |
| Age distribution | Shows how passenger ages are spread |
| Age distribution by survival | Compares ages of survivors and non-survivors |
| Fare distribution | Shows the skewed distribution of fares |
| Fare outlier boxplot | Highlights potential fare outliers |

---

## 💡 Key Findings

**Descriptive findings**

- 342 of 891 passengers survived, an overall survival rate of about 38.38%.
- Female passengers had a much higher survival rate (about 74.2%) than male passengers (about 18.9%).
- Survival rate decreased from 1st class (about 63%) to 2nd class (about 47%) to 3rd class (about 24%).
- Fare is strongly right-skewed, with a mean of 32.20 and a median of 14.45.
- 116 fare observations were flagged as potential outliers using the IQR method.
- Age has 177 missing values and Cabin has 687 missing values.
- No duplicate records were found.

**Statistical conclusions**

- Gender and survival showed a statistically significant association.
- Passenger class and survival showed a statistically significant association.
- The Mann-Whitney U test did not provide sufficient evidence of a significant difference in age distributions between survivors and non-survivors.

---

## 📂 Project Structure

```text
Titanic-Exploratory-Data-Analysis/
│
├── Titanic_EDA_Analysis.ipynb
└── README.md
```

> **Note:** If the Titanic dataset CSV file is not present in the repository, download the Titanic dataset (891 rows, 12 columns) and place it in the project folder before running the notebook. Make sure the file name matches the one used in the notebook.

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Vaishnavi5544/Titanic-Exploratory-Data-Analysis.git
```

### 2. Navigate to the project directory

```bash
cd Titanic-Exploratory-Data-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open and run the notebook

Open `Titanic_EDA_Analysis.ipynb` and run the cells in order.

---

## 📚 Learning Outcomes

Through this project, I practiced:

- Exploratory Data Analysis
- Data inspection and understanding
- Missing-value analysis
- Duplicate detection
- Data visualization
- Distribution analysis
- Outlier detection using the IQR method
- Categorical data analysis
- Hypothesis testing with the Chi-Square Test of Independence and the Mann-Whitney U Test
- Interpreting statistical results
- Communicating data-driven findings

---

## 🎯 Conclusion

This Titanic EDA project shows how exploratory analysis can reveal patterns, relationships, and data-quality issues in a real-world dataset.

The analysis found statistically significant associations between survival and both gender and passenger class. The age analysis did not provide sufficient statistical evidence of a significant difference between survivors and non-survivors.

The project also highlighted missing values and potential fare outliers that should be considered before any further analysis or predictive modeling.

---

## 🔮 Future Improvements

- Apply suitable techniques to handle missing values in Age, Cabin, and Embarked
- Explore additional variables such as family size (SibSp and Parch) and port of embarkation
- Perform further statistical analysis on other variables
- Build and evaluate a predictive model for survival
- Add more visualizations to support additional findings

---

## 👩‍💻 Author

**Vaishnavi Jadhav**

GitHub: [https://github.com/Vaishnavi5544](https://github.com/Vaishnavi5544)

---

⭐ If you found this project helpful, consider giving the repository a star on GitHub!
