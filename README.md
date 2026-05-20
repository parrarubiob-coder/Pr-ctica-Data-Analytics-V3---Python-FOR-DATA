# 📊 Bank Marketing Analysis with Python

## 🇪🇸 Spanish Version
➡️ [Read the Spanish version here](README_ES.md)

---

## 🛠️ Technologies & Tools

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)
![VSCode](https://img.shields.io/badge/VSCode-IDE-007ACC?style=for-the-badge&logo=visualstudiocode)

---

# 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objective](#-business-objective)
- [Datasets](#-datasets)
- [Project Workflow](#-project-workflow)
- [Data Cleaning](#-data-cleaning)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Visualizations](#-visualizations)
- [Key Insights](#-key-insights)
- [Business Recommendations](#-business-recommendations)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)

---

# 📌 Project Overview

This project consists of an **Exploratory Data Analysis (EDA)** performed using Python on direct marketing campaigns conducted by a Portuguese banking institution.

The main goal of the project is to analyze customer behavior and identify patterns related to term deposit subscriptions.

The analysis includes:

- Data cleaning and preprocessing
- Exploratory data analysis
- Statistical analysis
- Data visualization
- Business-oriented insights generation

---

# 🎯 Business Objective

Bank marketing campaigns aim to maximize customer conversion while optimizing resources and communication strategies.

This project seeks to:

- Identify customer profiles with higher conversion probability
- Detect variables influencing campaign success
- Understand customer behavior patterns
- Generate insights to improve future marketing campaigns

---

# 🗂️ Datasets

## 1️⃣ bank-additional.csv

Main dataset containing marketing campaign information.

### Main Variables

| Variable | Description |
|---|---|
| age | Customer age |
| job | Occupation |
| marital | Marital status |
| education | Education level |
| duration | Last contact duration |
| campaign | Number of contacts during campaign |
| previous | Number of previous contacts |
| poutcome | Previous campaign outcome |
| euribor3m | Euribor interest rate |
| y | Subscription result (yes/no) |

---

## 2️⃣ customer-details.xlsx

Excel dataset containing demographic and customer behavior information.

The file includes 3 worksheets corresponding to different years.

### Main Variables

| Variable | Description |
|---|---|
| Income | Annual income |
| Kidhome | Number of children at home |
| Teenhome | Number of teenagers at home |
| Dt_Customer | Customer registration date |
| NumWebVisitsMonth | Monthly website visits |
| ID | Unique customer identifier |

---

# ⚙️ Project Workflow

The project was developed following these main stages:

1. Data loading
2. Data cleaning and preprocessing
3. Dataset merging
4. Exploratory analysis
5. Statistical analysis
6. Data visualization
7. Business conclusions and recommendations

---

# 🧹 Data Cleaning

Main preprocessing tasks performed:

- Handling missing values
- Removing duplicates
- Standardizing column names
- Converting data types
- Formatting dates
- Merging datasets
- Detecting inconsistencies

### Example

```python
df.columns = df.columns.str.lower()

df['date'] = pd.to_datetime(df['date'])
