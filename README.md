# 🛒 Superstore Sales Data Analysis

## 📌 Project Overview

This project explores and analyzes the **Superstore sales dataset**, which is divided into three main tables:

* Customers
* Products
* Orders

The goal of this project is to **clean, merge, and analyze** the data to extract meaningful business insights about customer behavior, product performance, and regional trends.

---

## 🎯 Objectives

* Clean and preprocess messy real-world data
* Handle missing values and duplicates
* Merge multiple tables into a unified dataset
* Perform exploratory data analysis (EDA)
* Generate business insights from the data

---

## 🧹 Data Cleaning

### 1. Customers Table

* Removed duplicate `Customer ID`s
* Handled missing **Segment** values using group-based imputation
* Standardized IDs (trimmed spaces, consistent formatting)

### 2. Products Table

* Created a new feature `Category_from_ID` by extracting category codes from `Product ID`
* Filled missing `Category` values using the derived feature
* Checked for inconsistencies between original and derived categories

### 3. Orders Table

* Validated key columns (`Customer ID`, `Product ID`)
* Checked for missing or invalid entries

---

## 🔗 Data Merging

The three datasets were merged using:

* `Customer ID` → linking orders to customers
* `Product ID` → linking orders to products

Post-merge validation was performed to ensure:

* No unexpected row duplication
* Minimal missing values after joins

---

## 📊 Key Analysis & Insights

### 👤 Customer Analysis

* Identified top customers by total revenue
* Analyzed customer purchase frequency and average order value
* Observed that high revenue customers are not always high-frequency buyers

---

### 🌍 Regional Analysis

* Compared customer behavior across regions
* Found that **top customers are generally region-specific**, with limited overlap across regions

---

### 🛍️ Product & Category Insights

* Determined which **category dominates each region**
* Observed variation in category performance across regions, indicating localized demand patterns

---

### 📦 Product Distribution

* Identified **region-specific products** (products sold in only one region)
* Found that some products are localized, while others are distributed globally

---

## ⚠️ Data Quality Insights

* Missing values in **Segment** and **Category** required careful handling

* The **Customers table** posed the most challenges due to:

  * Missing values
  * Duplicate records
  * Inconsistent data

* Some missing values were imputed, which may introduce minor bias in analysis

---

## 🧠 Key Learnings

* Data cleaning is an iterative process, not a one-time step
* Merging datasets can introduce hidden issues (e.g., duplication, null joins)
* Feature engineering (like extracting category from IDs) can recover lost information
* Always validate data before drawing conclusions

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* Jupyter Notebook

---

## 📈 Future Improvements

* Add visualization dashboards (Matplotlib / Seaborn / Power BI)
* Incorporate profit analysis (if data available)
* Perform customer segmentation (e.g., VIP, Regular, Low-value)
* Build predictive models for sales forecasting

---

## 📎 Project Structure

```
├── data/
│   ├── customers.csv
│   ├── products.csv
│   └── orders.csv
├── notebooks/
│   └── analysis.ipynb
├── README.md
```

---

## ✨ Conclusion

This project demonstrates a complete **data analysis workflow**, from raw messy data to actionable insights. It highlights the importance of data cleaning, validation, and thoughtful analysis in real-world datasets.

---
