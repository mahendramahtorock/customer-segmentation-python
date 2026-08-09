# Customer Segmentation and Marketing Analysis using Python

Author: Mahendra Kumar Mahto

## About this project

I worked on this project to understand customer spending behavior using Python. The dataset had information about customer income, age, product spending, purchase channels and marketing campaign responses. My goal was to find useful patterns in this data and divide customers into groups so that a business can plan marketing in a better way.

I used Python, Pandas, NumPy, Matplotlib and Seaborn for this project.

## Problem

When we look at all customers together as one big group, it becomes hard to answer simple business questions like:

- Which customers are spending the most money?
- Which customers are not engaged much?
- Which products are selling well?
- Which purchase channel is used the most?
- Which marketing campaign worked better than others?

So there was a need to break down the customer data into smaller groups and study it properly.

## What I did

I worked with data of 2,240 customers. After cleaning the data, I created a simple rule based segmentation. I did not use machine learning or clustering for this, because I have not learned that yet. Instead, I divided customers into four groups based on how much they spend:

- Low Value
- Medium Value
- High Value
- VIP

This was done using spending percentiles in Pandas.

## Steps I followed

1. Loaded the dataset in Pandas and checked its structure.
2. Cleaned the data. Checked for missing values, duplicate rows, fixed the income column, converted the customer date column to proper date format, and checked for wrong age and income values.
3. Created new columns that were useful for analysis, like Age, Children, Total Spending, Total Purchases and Campaigns Accepted.
4. Did exploratory analysis on age, income, education, marital status, product spending, purchase channels and campaign performance.
5. Divided customers into four spending based segments and compared them.

## What I found

### Customer value

Each of the four groups had close to 25 percent of the total customers.

| Segment | Customers | Average Spending | Average Purchases |
|---|---|---|---|
| Low Value | 560 | 39.26 | 4.31 |
| Medium Value | 561 | 184.57 | 8.27 |
| High Value | 559 | 709.82 | 17.59 |
| VIP | 560 | 1,490.48 | 19.99 |

VIP customers spend almost 38 times more than Low Value customers.

What can be done: Keep VIP customers happy with loyalty offers and premium deals so they do not leave.

### High Value customers have room to grow

High Value customers spend 709.82 on average and make about 17.59 purchases. Their average income is 60,419, while VIP customers have an average income of 75,238.

What can be done: Offer bundles and personal offers to these customers so some of them can move up to VIP.

### Low Value customers need attention

Low Value customers are also about 25 percent of all customers, but they spend only 39.26 on average and make just 4.31 purchases.

What can be done: Send them discounts and simple offers to bring them back and increase their purchases.

### Products that sell the most

Wine and Meat together make up about 77.73 percent of all product spending.

What can be done: Keep promoting these two categories and use them to introduce customers to other products.

### Purchase channels

Store purchases are the highest, at about 46.18 percent. Web purchases are about 32.58 percent and Catalog purchases are about 21.23 percent.

What can be done: Keep the store channel strong, and try offers that push more customers towards Web and Catalog.

### Marketing campaigns

The latest campaign got a response from 334 customers, which is about 14.91 percent. The best campaign before that got 167 responses, about 7.46 percent.

What can be done: Study what type of customers responded to the successful campaigns and use that information for future campaigns.

## Why this matters

Customer data is only useful if it helps in making better decisions. This project helps in moving away from treating all customers the same way, and instead gives a simple plan for each group:

- VIP customers: Keep them
- High Value customers: Help them grow
- Medium Value customers: Sell them more products
- Low Value customers: Bring them back

## Possible impact

- 560 VIP customers can be given priority for retention offers.
- 560 Low Value customers can be targeted with offers to bring them back.
- Wine and Meat make up 77.73 percent of product spending, so they are important for cross selling.
- 46.18 percent of purchases happen in stores, so this channel needs attention.
- The last campaign had a response rate of 14.91 percent, which can be used as a target for future campaigns.

These are just findings from the data. No real marketing test was done, so these are opportunities and not confirmed results.

## Problems I faced and how I solved them

**CSV file loading wrong**
At first the file loaded as one single column. I checked the file and fixed the separator so each column loaded properly.

**Wrong data types**
Some columns like income and date were not in the right format. I converted them using Pandas and checked the types again.

**Date column error**
The date column gave errors because dates were written as day-month-year. I fixed this using Pandas date functions.

**Wrong age values**
A few customers had age values that did not make sense. I found these values and removed them only from the age related charts, not from the full dataset.

**High income values**
Some customers had very high income compared to others. I checked this using a boxplot before using income in my analysis.

**Choosing how to group customers**
I first thought of using clustering, but I have not learned that method yet. So I used a simple rule based method with spending percentiles instead. This was easier to explain and still gave useful groups.

## Tools used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Result

This project turned raw customer data into useful information. It shows the high value customers, the low engagement customers, the best selling products, the strongest purchase channel and the difference between marketing campaigns. It also gives four clear customer groups that a business can use for better marketing decisions.

## Files in this project

```
Customer-Segmentation-Python/
│
├── Customer_Segmentation_Marketing_Analysis.ipynb
├── README.md
└── images/
    ├── age_distribution.png
    ├── product_spending.png
    ├── campaign_performance.png
    └── customer_segments.png
```
