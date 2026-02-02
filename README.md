# 📘 Understanding Your Data – Asking Basic Questions

## 📌 Project Overview

This repository contains a Jupyter Notebook focused on **Exploratory Data Analysis (EDA)**.
The goal of the notebook is to understand the structure, quality, and basic statistical
properties of the dataset before applying any machine learning models.

Notebook file:
- `Understanding_your_data_(asking_basic_questions).ipynb`

---

## 🎯 Objectives of the Notebook

The notebook answers fundamental questions such as:

- What are the available features in the dataset?
- What data types do these features have?
- Which features are numeric vs non-numeric?
- Are there missing values?
- How are numeric features related to each other?

---

## 🔍 Correlation Analysis

During EDA, correlation analysis was performed using:


### ⚠️ Observed Issue

The above command raised the following error:


---

## 🧠 Explanation

- Correlation is a **mathematical operation** that is defined only for numeric values.
- The dataset contains **non-numeric columns** (e.g., names or categorical text).
- When `df.corr()` encounters text data, pandas attempts to convert it to float,
  which leads to a conversion error.

This behavior is expected and indicates mixed data types in the dataset.

---

## ✅ Correct Approach

To compute correlation correctly, only numeric columns should be used.

### Recommended solution:


This ensures:
- Only numerical features are included
- The correlation matrix is computed correctly
- The analysis follows standard data science practices

---

## 🔎 Data Type Inspection

To understand why the error occurs, data types can be checked using:


Columns with `object` or `string` data types are excluded from correlation analysis.

---

## 📌 Key Takeaways

- Exploratory Data Analysis is essential before modeling
- Not all features are suitable for statistical operations
- Numeric and non-numeric data must be handled differently
- Proper filtering of features prevents analytical errors

---

## 🛠 Tools & Libraries Used

- Python
- Pandas
- Jupyter Notebook

---

## ✅ Conclusion

This notebook demonstrates the importance of understanding data structure
and data types during the early stages of analysis. Handling numeric and
categorical features correctly leads to more reliable and interpretable results.

---

📎 This repository is intended for learning, EDA practice, and foundational
data analysis workflows.
