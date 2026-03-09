# Retail Store Performance and Holiday Sales Analysis

## 🔎 Overview

Retail businesses face constant fluctuations in demand driven by seasonality, promotions, holidays, and external factors such as weather. Understanding these patterns is critical for optimizing inventory planning, staffing, and marketing strategies.

This project analyzes over 421,000 retail sales records across 45 stores and multiple departments to uncover patterns in sales performance and identify how **holidays, promotions, and store characteristics influence retail demand**.

Through **exploratory data analysis and feature engineering**, the project provides insights into store performance, department trends, and the impact of holidays and promotional markdowns on weekly sales.

The goal is to demonstrate how data analytics can help retailers make data-driven operational and merchandising decisions.

## 🔐 Business Problem

Retailers must constantly answer key operational questions:

* Which stores generate the highest sales?
* How do holiday periods influence retail demand?
* Which departments drive the majority of revenue?
* How do promotional markdowns impact sales performance?
* Do external factors such as temperature or economic indicators influence retail demand?

Without clear insights into these patterns, retailers risk:

* overstocking or understocking inventory
* inefficient staffing
* poorly timed promotions
* missed sales opportunities during peak demand periods

This analysis aims to uncover systematic sales patterns that can guide better retail decision-making.

## 📊 Dataset

The dataset combines three related retail datasets containing store characteristics, external features, and sales transactions.

| Dataset        | Description                                                                                        |
| -------------- | -------------------------------------------------------------------------------------------------- |
| `train.csv`    | Weekly sales by store and department                                                               |
| `features.csv` | External variables including temperature, fuel price, CPI, unemployment, and promotional markdowns |
| `stores.csv`   | Store characteristics including store type and size                                                |

These datasets were merged to create a unified dataset with:

* 421,570 observations
* 45 stores
* multiple departments
* weekly sales records across multiple years

The merged dataset includes features such as:

* store size
* department
* weekly sales
* promotional markdown values
* CPI and unemployment
* holiday indicator
* temperature

The datasets were merged using store ID, date, and holiday indicator to align sales and external variables. 

## 📍 Methodology

The analysis consists of four major stages.

### 1. Data Preparation

The three datasets were merged into a single dataset using store ID and date.

Key preprocessing steps included:

* merging store features with sales data
* converting date columns to datetime format
* extracting time features such as month and year
* handling missing values by filling markdown values with zero

After cleaning, the dataset was sorted chronologically and indexed by date to enable time-series analysis. 

### 2. Store Performance Analysis

Total weekly sales were aggregated by store to identify top-performing locations.

A store-level sales comparison highlights significant differences in performance across the retail network.

The bar chart below illustrates total sales by store, showing that some stores generate significantly higher revenue than others.

<img width="848" height="556" alt="image" src="https://github.com/user-attachments/assets/11b8e059-d5e1-4365-8aac-a527e0acddda" />

### 3. Holiday and Promotion Analysis

To measure holiday effects, a **Holiday Sales Impact Index** was created by comparing:

```
Average Holiday Sales / Average Non-Holiday Sales
```

<img width="863" height="555" alt="image" src="https://github.com/user-attachments/assets/28dc8d10-aedb-40d0-a7f6-9ea2451f69d6" />

This metric quantifies how much holidays increase or decrease store sales.

Additional analysis evaluated:

* average weekly sales by store type
* promotional markdown activity during holiday periods
* average markdown spending by store type

Stores of Type A typically generated the highest sales and showed stronger holiday uplift compared to smaller stores.

<img width="868" height="525" alt="image" src="https://github.com/user-attachments/assets/7e2e8fb7-e9cf-41bb-93f2-a9218f25cd05" />

### 4. Department and Seasonality Analysis

Department-level analysis identified the top four departments by total sales, then analyzed their monthly sales patterns.

<img width="1357" height="860" alt="Screenshot 2026-03-09 at 4 17 07 AM" src="https://github.com/user-attachments/assets/db316259-aa53-40d6-a75a-e79a5b1b70e3" />

This revealed seasonal patterns in product demand across departments.

Time-series analysis also compared:

* total weekly sales over time
* average temperature over time

to explore whether weather conditions correlate with retail demand.

## 🔑 Key Insights

### 1. Significant differences in store performance

Some stores generate substantially higher sales volumes, indicating differences in location, store size, and local demand conditions.

These insights can guide store expansion and investment decisions.

### 2. Holidays increase retail sales

The Holiday Sales Impact Index shows that many stores experience 10–18% higher sales during holiday periods**, confirming the importance of seasonal demand spikes.

Holiday periods therefore represent critical revenue opportunities.

### 3. Store size and type influence sales

Store Type A consistently generates the highest weekly sales compared to Types B and C, suggesting that store size and format significantly influence revenue potential.

### 4. Promotions intensify during holidays

Promotional markdown values are significantly higher during holiday periods, indicating that retailers use aggressive discount strategies to maximize sales during peak demand.

### 5. Certain departments drive most revenue

A small subset of departments accounts for a disproportionate share of total sales.

Understanding department-level performance can help optimize product assortment, inventory allocation, and promotional strategies.

## ✍️ Business Recommendations

### 1. Optimize inventory for holiday demand

Retailers should increase inventory levels for top-performing departments during holiday periods to avoid stockouts and maximize revenue.

### 2. Allocate marketing budget toward high-performing stores

Stores with consistently high sales should receive greater marketing investment to further expand their revenue potential.

### 3. Use targeted promotions instead of broad discounts

Analyzing markdown performance by department can help retailers identify which products respond most strongly to discounts.

### 4. Improve demand forecasting

Seasonality and department-level demand patterns should be integrated into forecasting models to improve operational planning.

## ⚙ Tools & Technologies

* Python
* Data preprocessing (Pandas, NumPy)
* Data visualization (Matplotlib, Seaborn)
* Exploratory data analysis (EDA)
* Feature engineering
* Time-series trend analysis
