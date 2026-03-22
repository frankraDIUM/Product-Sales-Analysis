# Product-Sales-Analysis
This project analyzes a product sales dataset of 15,000 records to uncover patterns in customer behavior, sales methods, and revenue generation.

<p align="center">
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/Relatonship%20between%20revenue%20and%20sold.png"
</p>

<p align="center">
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/customer_engagement.png" width="45%" />
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/customer_behaviour.png" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/revenue_change.png" width="45%" />
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/revenue_trend.png" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/average_metrics.png" width="45%" />
  <img src="https://github.com/frankraDIUM/Product-Sales-Analysis/blob/main/customer_retention.png" width="45%" />
</p>

## 1. Data Validation & Cleaning

### Dataset Overview

* **Records:** 15,000
* **Columns:** 8
* Includes sales methods, customer details, and product performance.

### Key Columns

* `week` – Week of sale (1–6)
* `sales_method` – Email, Call, Email + Call
* `customer_id` – Unique identifier
* `nb_sold` – Number of products sold
* `revenue` – Revenue per transaction
* `years_as_customer` – Customer tenure
* `nb_site_visits` – Website visits (last 6 months)
* `state` – Customer location

### Cleaning Steps

* **Sales Method**

  * Standardized to: `Email`, `Call`, `Email + Call`

* **Revenue**

  * ~7% missing values (1,074 rows)
  * Filled using:

    ```
    avg_price = total_revenue / total_products_sold
    estimated_revenue = nb_sold * avg_price
    ```

* **Years as Customer**

  * Outliers capped at **40 years**

* **Duplicates**

  * None found

### Post-Cleaning Checks

*  No missing values
*  No duplicates
*  Consistent categories
*  Outliers handled

---

## 2. Exploratory Data Analysis (EDA)

### Key Insights

* **Products Sold**

  * Right-skewed distribution
  * Most transactions involve fewer items

* **Sales Methods**

  * Most used: `Email` and `Email + Call`
  * Least used: `Call`

* **Revenue vs Products Sold**

  * Positive correlation
  * Some variability → possible pricing/discount differences

---

## 3. Business Metric

### Average Revenue per Product

```
Average Revenue per Product = Total Revenue / Total Products Sold
```

* **Current Value:** `$9.28`

### Why it Matters

* Evaluates pricing effectiveness
* Compares performance across sales methods
* Tracks profitability over time

---

## 4. Recommendations

* **Focus on Top Sales Channels**

  * Optimize `Email` and `Email + Call`

* **Review Pricing Strategy**

  * Investigate revenue variability (discounts, pricing differences)

* **Track Key Metric**

  * Monitor average revenue per product regularly

---

## Summary

* Data required minimal cleaning (standardization, missing values, outliers)
* Sales are mostly low-volume but frequent
* Email-based methods dominate sales
* Revenue scales with quantity but varies due to pricing
* Key metric: **$9.28 revenue per product**

---
