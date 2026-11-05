# Small-Business-Profitability-Analysis
Small Business Profitability Analysis
Project ID: DA-019
Domain: Business Analytics

An analytical project to study sales, product costs, customer discounts, and return patterns for a retail small business to understand profitability and identify products and seasons that yield the best margins.

Overview & Problem Statement
A small retail business knows its gross sales figures, but revenue alone does not tell the full story. Products with high sales revenue may carry high procurement costs, high discount rates, or high return rates that reduce actual profits.

This project analyzes a dataset of 1,400 transactions across 5 product categories (Electronics, Apparel, Home & Kitchen, Stationery, and Personal Care) to:

Compute Net Revenue, Total COGS, Net Profit, and Profit Margin (%).
Compare profitability across categories.
Examine how discounts affect margin percentages.
Identify seasonal sales trends across 12 months.
Rank the most and least profitable products.
Formulas & Business Rules
Key Rule: Revenue is not profit. Profit is calculated after deducting product costs (COGS) and accounting for discounts and returns.

Gross Revenue = 
Unit Price
×
Units Sold
Discount Amount = 
Gross Revenue
×
(
Discount Percent
/
100
)
Net Revenue = 
Gross Revenue
−
Discount Amount
 (0 if returned)
Total COGS = 
Unit Cost
×
Units Sold
 (0 if returned and restocked)
Net Profit = 
Net Revenue
−
Total COGS
Profit Margin (%) = 
(
Net Profit
/
Net Revenue
)
×
100
Visualizations
1. Category-wise Net Revenue vs Net Profit
Category Revenue vs Profit Electronics generates the highest revenue, but Stationery and Personal Care deliver significantly higher profit margins (>50%).

2. Monthly Revenue, Profit & Margin Dynamics
Monthly Trends Sales peak in Q4 during festive shopping, while base margins remain steady throughout the year.

3. Impact of Discounts on Profit Margin
Discount Impact Discounts above 20% lead to steep margin drops (falling from ~55% down to under 25%).

4. Product Profit Margin Comparison (Top 5 vs Bottom 5)
Product Rankings High-margin stationery items deliver over 60% margin, while high-ticket electronics like gaming keyboards have margins around 32-35%.

Project Structure
Small-Business-Profitability-Analysis/
├── charts/                           # Generated PNG charts
│   ├── 01_category_revenue_profit.png
│   ├── 02_monthly_profit_trend.png
│   ├── 03_discount_vs_profit_margin.png
│   └── 04_top_bottom_products_margin.png
├── data/
│   ├── generate_dataset.py           # Dataset generator script
│   └── small_business_sales.csv      # Sales data (1,400 transactions)
├── docs/
│   ├── PROJECT_REPORT.md             # Detailed academic project report
│   └── VIVA_CHEAT_SHEET.md           # Common viva questions & answers
├── notebooks/
│   └── profitability_analysis.ipynb  # Main Jupyter Notebook
├── src/
│   ├── clean_data.py                 # Data cleaning and feature extraction
│   ├── metrics.py                    # Financial formula implementations
│   └── visualize.py                  # Matplotlib plotting scripts
└── README.md
How to Run
Generate Dataset (if not already present):

python data/generate_dataset.py
Run Scripts & Generate Charts:

python src/visualize.py
Open Jupyter Notebook:

jupyter notebook notebooks/profitability_analysis.ipynb
