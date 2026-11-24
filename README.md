# Customer Summary: Exploratory Data Analysis

Exploratory analysis of an electronics retail dataset (127k order lines, 63k customers, Canada / US / UK / Germany, 2016-2022) using Python, Pandas, Matplotlib and Seaborn.

## Files
- `customer_eda.ipynb`: the full analysis (read, clean, 29 charts with insights)
- `customer_summary.csv`: dataset (place it in the same folder as the notebook)

## Run
```
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook customer_eda.ipynb
```

## What the notebook covers
1. Data understanding and quality checks
2. Cleaning (duplicates, invalid ratings, placeholder income, constant columns)
3. Sales over time, products and regions
4. Order value distributions and outliers
5. Customer profile and loyalty tiers
6. Satisfaction and shipping analysis, correlation heatmap

## Key findings
- **2020 revenue peak** ($100M) comes from 345 bulk orders of 50+ units, not more customers. 2022 has Q1 only.
- **TV & Video Gaming and Computers** make up about 80% of revenue, with the same mix in every country.
- **Revenue is right-skewed:** mean is about double the median, and the top 10% of orders give about 42% of revenue.
- **Shipping drives satisfaction:** orders shipped in 5+ days average 2.63 stars vs 3.39 for faster ones; delayed delivery is the top complaint.
- **Demographics show little signal:** gender, area type, country and loyalty tier are near-equal splits.

## Data notes
- `INCOME = 0` is a placeholder (all College-level customers), treated as missing.
- Cleaning removes 333 rows (96 duplicates, 237 invalid ratings).
- The data appears synthetic (cost is exactly 85% of price on every row).
