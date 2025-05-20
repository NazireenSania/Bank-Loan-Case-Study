# 🏦 Bank Loan Case Study – Excel-Based Data Analysis

This project analyzes customer loan application data to explore financial patterns, handle missing values, detect data imbalance, and identify default risk segments. The analysis was performed in **Microsoft Excel** and focuses on practical data preprocessing and EDA techniques.

---

## 📂 Project Structure

- 📊 **Tool Used:** Microsoft Excel  
- 📁 **Datasets Used:**  
  - `application_data`: Contains current loan applications and customer attributes (122 columns)  
  - `previous_application`: Historical loan details and repayment history  
  - `columns_description`: Metadata explaining each variable  

> **Primary analysis was performed on `application_data` dataset.**

---

## 🧹 Data Cleaning

- Removed duplicate rows using Excel’s "Remove Duplicates" tool.
- Dropped columns with excessive missing values.
- Handled missing values using:
  - **Mean** for normally distributed data
  - **Median** for skewed distributions (based on skewness)
  - **Mode** for categorical variables


```excel
=IF(SKEW(A2:A100)<1, AVERAGE(A2:A100), MEDIAN(A2:A100))
