# Decodelabs_Task01

# Data Science Project 1: Advanced EDA & Feature Engineering

## Overview

This project focuses on performing Advanced Exploratory Data Analysis (EDA) and Feature Engineering on an e-commerce dataset. The objective is to transform raw data into a clean, structured, and machine-learning-ready dataset by handling missing values, treating outliers, and creating new predictive features.

## Objectives

* Analyze the dataset structure and data quality.
* Handle missing values using statistical imputation techniques.
* Detect and treat outliers using the Interquartile Range (IQR) method.
* Engineer new features from existing columns.
* Perform exploratory data analysis through visualizations.
* Generate a cleaned dataset suitable for machine learning applications.

---

## Dataset Information

The dataset contains customer order information from an e-commerce platform.

### Features

| Column Name     | Description                 |
| --------------- | --------------------------- |
| OrderID         | Unique order identifier     |
| Date            | Date of order               |
| CustomerID      | Unique customer identifier  |
| Product         | Product purchased           |
| Quantity        | Number of units purchased   |
| UnitPrice       | Price per unit              |
| ShippingAddress | Delivery location           |
| PaymentMethod   | Payment mode used           |
| OrderStatus     | Current order status        |
| TrackingNumber  | Shipment tracking ID        |
| ItemsInCart     | Total items in cart         |
| CouponCode      | Discount coupon used        |
| ReferralSource  | Customer acquisition source |
| TotalPrice      | Total order value           |

---

## Project Workflow

### 1. Data Loading

* Imported dataset using Pandas.
* Examined data types and dataset dimensions.

### 2. Missing Value Handling

* Identified missing values using `isnull().sum()`.
* Filled missing values in the `CouponCode` column with `"No Coupon"`.

### 3. Outlier Detection and Treatment

* Applied the Interquartile Range (IQR) method.
* Detected outliers in numerical columns.
* Treated outliers using Winsorization (`numpy.clip()`).

### 4. Feature Engineering

Created the following new features:

#### OrderMonth

Extracted month from the order date.

#### OrderYear

Extracted year from the order date.

#### AvgItemValue

Calculated average value per item.

Formula:

AvgItemValue = TotalPrice / Quantity

#### CartEfficiency

Calculated purchase efficiency.

Formula:

CartEfficiency = Quantity / ItemsInCart

### 5. Exploratory Data Analysis

Generated visualizations for:

* Missing values
* Total price distribution
* Outlier analysis
* Payment method distribution
* Order status distribution
* Product popularity

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Google Colab

---

## Installation

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

---

## Running the Project

1. Open Google Colab or Jupyter Notebook.
2. Upload the dataset file.
3. Run all notebook cells sequentially.
4. Review generated visualizations.
5. Export the cleaned dataset.

---

## Output

The project generates:

* Cleaned dataset (`Cleaned_Dataset.csv`)
* EDA visualizations
* Engineered features
* Outlier-treated dataset

---

## Key Learnings

* Data cleaning techniques
* Missing value imputation
* Outlier detection using IQR
* Feature engineering
* Exploratory Data Analysis (EDA)
* Data preprocessing for machine learning

---

## Future Improvements

* Apply KNN Imputation for advanced missing-value treatment.
* Build predictive machine learning models.
* Perform feature selection.
* Create interactive dashboards using Power BI or Tableau.

---

## Author

Praveen

Data Science Industrial Training Project 1

DecodeLabs Batch 2026
