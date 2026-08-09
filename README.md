# Customer Segmentation & Marketing Analysis Using Python

## Project Overview

This project analyzes customer data to understand spending behavior, purchasing patterns, marketing campaign responses, and customer value.

The main goal was to identify different customer groups and understand how the business can use customer data to improve marketing decisions.

The analysis was performed using Python, Pandas, NumPy, Matplotlib, and Seaborn.

---

## Problem Statement

The company has customer information such as income, age, product spending, purchase channels, and campaign responses.

However, looking at all customers as one group makes it difficult to understand:

- Which customers are the most valuable?
- Which customers need more engagement?
- Which products generate the most spending?
- Which purchase channels are most important?
- Which marketing campaigns perform better?

The business needs a simple way to understand customer behavior and target different customer groups more effectively.

---

## Objective

The main objectives of this project were to:

- Analyze customer demographics and spending behavior.
- Understand product-wise spending.
- Compare different purchase channels.
- Analyze marketing campaign responses.
- Identify high-value customers.
- Create customer segments based on spending behavior.
- Provide practical recommendations for better customer targeting.

---

## Solution

I analyzed **2,240 customer records** using Python and created a rule-based customer segmentation approach.

Customers were divided into four groups based on their total spending:

| Segment | Business Meaning |
|---|---|
| Low Value | Customers with relatively low spending |
| Medium Value | Customers with moderate spending |
| High Value | Customers with strong spending |
| VIP | Customers with very high spending |

The segmentation was created using spending percentiles rather than machine learning or clustering.

---

## Analysis Approach

The project followed these steps:

### 1. Data Loading

Loaded the marketing campaign dataset into Pandas and checked its structure.

### 2. Data Cleaning

- Checked missing values.
- Checked duplicate records.
- Converted income into a numeric format.
- Converted customer dates into datetime format.
- Checked unrealistic age values and income outliers.

### 3. Feature Engineering

Created useful business variables:

- `Age`
- `Children`
- `Total_Spending`
- `Total_Purchases`
- `Campaigns_Accepted`

### 4. Exploratory Data Analysis

Analyzed:

- Customer age
- Income
- Education
- Marital status
- Product spending
- Purchase channels
- Marketing campaign performance
- Income vs spending
- Age vs spending
- Correlations
- Top 10 high-value customers

### 5. Customer Segmentation

Customers were divided into:

- Low Value
- Medium Value
- High Value
- VIP

The segments were then compared based on income, spending, and purchase activity.

---

# Key Insights

## 1. Customer Value

The analysis identified four customer groups, each representing roughly **25% of the customer base**.

| Segment | Customers | Avg. Spending | Avg. Purchases |
|---|---:|---:|---:|
| Low Value | 560 | 39.26 | 4.31 |
| Medium Value | 561 | 184.57 | 8.27 |
| High Value | 559 | 709.82 | 17.59 |
| VIP | 560 | 1,490.48 | 19.99 |

VIP customers spend around **38 times more** than Low Value customers on average.

### Business Recommendation

Focus on retaining VIP customers through loyalty rewards, personalized offers, and premium products.

---

## 2. Growth Opportunity

High Value customers spend an average of **709.82** and make around **17.59 purchases**.

Their average income is also **60,419**, compared with **75,238** for VIP customers.

### Business Recommendation

Use cross-selling, bundles, and personalized offers to increase spending among High Value customers and move suitable customers toward the VIP segment.

---

## 3. Re-engagement Opportunity

Low Value customers represent around **25% of the customer base**, but their average spending is only **39.26**.

They also make only **4.31 purchases** on average.

### Business Recommendation

Use targeted discounts, bundles, and re-engagement campaigns to increase their purchase frequency.

---

## 4. Product Opportunity

Wine and Meat are the strongest product categories.

Together, they contribute approximately **77.73% of total product spending**.

### Business Recommendation

Continue promoting these strong categories and use them to cross-sell lower-performing products.

---

## 5. Purchase Channel Opportunity

Store purchases are the strongest channel, accounting for around **46.18% of total recorded purchases**.

Web purchases account for around **32.58%**, while Catalog purchases account for around **21.23%**.

### Business Recommendation

Continue strengthening the Store channel while testing targeted offers to increase Web and Catalog purchases.

---

## 6. Marketing Campaign Opportunity

The latest campaign received responses from **334 customers**, or approximately **14.91% of the customer base**.

The strongest previous campaign received **167 responses**, or around **7.46%**.

### Business Recommendation

Study the characteristics of customers responding to successful campaigns and use those characteristics to improve future campaign targeting.

---

# Why This Analysis Matters

Customer data is useful only when it helps the business make better decisions.

This project helps the business move from a **one-size-fits-all marketing approach** toward more targeted strategies.

For example:

- **VIP → Retain**
- **High Value → Grow**
- **Medium Value → Cross-sell**
- **Low Value → Re-engage**

This allows marketing efforts to be focused on the customers and products where there is a clear opportunity.

---

# Potential Business Impact

The analysis identifies several areas where the business can improve:

- **560 VIP customers** can be prioritized for retention.
- **560 Low Value customers** can be targeted with re-engagement offers.
- **77.73% of product spending** comes from Wine and Meat, making them important categories for cross-selling.
- **46.18% of purchases** happen through stores, highlighting the importance of this channel.
- The latest campaign achieved a **14.91% response rate**, providing a useful benchmark for future campaigns.

These are opportunities identified from the dataset. They are **not claimed as actual revenue improvements**, because no real-world marketing experiment was conducted.

---

# Challenges Faced & How I Solved Them

## 1. CSV Data Loading Issue

### Problem

Initially, the dataset was loaded incorrectly and appeared as one long column.

### Solution

I checked the structure of the source file and corrected the CSV separator so that each field was loaded into its proper column.

---

## 2. Data Type Issues

### Problem

Some columns were not in the correct format for analysis.

For example, income needed to be treated as a numerical variable and the customer date needed to be treated as a date.

### Solution

I converted the columns using Pandas and checked their data types before continuing with the analysis.

---

## 3. Date Conversion Error

### Problem

The `Dt_Customer` column initially caused errors during date conversion because the dates were stored in day-month-year format.

### Solution

I converted the column using Pandas datetime functions and handled invalid values safely.

---

## 4. Unrealistic Age Values

### Problem

Some customer records resulted in unrealistic ages.

### Solution

Instead of allowing these values to affect the analysis, I identified and flagged unrealistic ages and excluded them from age-based visual analysis.

---

## 5. Income Outliers

### Problem

A few customers had unusually high income values that could affect averages.

### Solution

I used distribution analysis and a boxplot to identify potential income outliers before interpreting income-based results.

---

## 6. Choosing a Segmentation Method

### Problem

I initially considered clustering, but clustering is a machine learning technique that I had not learned yet.

### Solution

I used a **rule-based segmentation approach with Pandas** instead.

Customers were grouped using spending percentiles into Low Value, Medium Value, High Value, and VIP segments.

This kept the project focused on Python and business analysis while still producing useful customer segments.

---

# Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

# Project Outcome

This project helped turn raw customer data into practical business insights.

The analysis identified:

- High-value customers
- Low-engagement customers
- High-performing products
- Strong and weak purchase channels
- Marketing campaign differences
- Four customer value segments

The final recommendations can help the business improve **customer retention, targeted marketing, cross-selling, and customer engagement**.

---

## Project Structure

```text
Customer-Segmentation-Python/
│
├── Customer_Segmentation_Marketing_Analysis.ipynb
├── README.md
└── images/
    ├── age_distribution.png
    ├── product_spending.png
    ├── campaign_performance.png
    └── customer_segments.png



