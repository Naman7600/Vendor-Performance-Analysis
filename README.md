# 📊 Vendor Performance Analysis

An end-to-end **Data Analytics** project that analyzes procurement, sales, profitability, inventory, and vendor performance using Python and SQL.

The project combines multiple operational datasets into a single analytical table and extracts business insights through exploratory data analysis, visualization, statistical analysis, and dashboarding.

---

# Project Overview

Organizations purchase products from multiple vendors, but not every vendor contributes equally to revenue or profitability.

This project aims to answer important business questions such as:

- Which vendors contribute the most to total sales?
- Which brands generate the highest revenue?
- Which products have high margins but low sales?
- How concentrated are purchases among vendors?
- Does bulk purchasing reduce the unit purchase price?
- How much capital is locked in unsold inventory?
- Is there a statistically significant difference in profit margins between top-performing and low-performing vendors?

---

# Dataset

The project integrates information from multiple operational tables including:

- Purchases
- Sales
- Purchase Prices
- Vendor Invoice
- Beginning Inventory
- Ending Inventory

These datasets are merged to create a consolidated **vendor_sales_summary** table for analysis. :contentReference[oaicite:3]{index=3}

---

# Data Engineering

The project first builds a unified analytical dataset by joining procurement and sales information.

Additional business metrics are created, including:

- Gross Profit
- Profit Margin (%)
- Stock Turnover
- Sales-to-Purchase Ratio

These transformations are implemented in the preprocessing pipeline before loading the final analytical table. :contentReference[oaicite:4]{index=4}

---

# Tech Stack

- Python
- SQL (SQLite)
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- DuckDB
- Jupyter Notebook

---

# Project Workflow

```text
Raw Tables
     │
     ▼
SQL Data Extraction
     │
     ▼
Vendor Sales Summary Creation
     │
     ▼
Data Cleaning
     │
     ▼
Feature Engineering
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Business Analysis
     │
     ▼
Statistical Testing
     │
     ▼
Dashboard & Insights
```

---

# Feature Engineering

The following metrics were created for business analysis:

- Gross Profit
- Profit Margin (%)
- Stock Turnover
- Sales-to-Purchase Ratio
- Unit Purchase Price
- Purchase Contribution (%)
- Cumulative Purchase Contribution
- Unsold Inventory Value
- Order Size Categories

---

# Exploratory Data Analysis

Performed:

- Summary Statistics
- Data Type Inspection
- Count Plots
- Correlation Heatmap

---

# Vendor Performance Analysis

The project evaluates vendor performance by calculating:

- Total Purchase Value
- Total Sales Value
- Gross Profit
- Purchase Contribution (%)

It also identifies:

- Top Vendors by Sales
- Top Vendors by Purchase Contribution

Visualizations include:

- Horizontal Bar Charts
- Pareto Chart
- Donut Chart

---

# Brand Performance Analysis

Brand-level analysis includes:

- Top Selling Brands
- High Profit Margin & Low Sales Brands

A scatter plot is used to identify products that generate high margins but comparatively lower sales, helping identify promotional opportunities.

---

# Procurement Analysis

The procurement analysis measures:

- Vendor Purchase Contribution
- Cumulative Purchase Contribution
- Vendor Dependency
- Purchase Concentration

It also investigates whether increasing purchase quantity reduces unit purchase price.

Purchase quantities are segmented into:

- Small Orders
- Medium Orders
- Large Orders

using quantile-based grouping (`pd.qcut`).

---

# Inventory Analysis

Inventory performance is evaluated by calculating:

- Unsold Inventory Value

Formula:

```
Unsold Inventory Value =
(Total Purchase Quantity − Total Sales Quantity)
× Purchase Price
```

The project identifies vendors contributing the highest amount of capital locked in unsold inventory.

---

# Statistical Analysis

The project includes inferential statistics in addition to descriptive analytics.

## Confidence Interval

Calculated **95% Confidence Intervals** for the mean profit margin of:

- Top-performing vendors
- Low-performing vendors

---

## Hypothesis Testing

Welch's Two Sample T-Test was performed to compare profit margins.

### Null Hypothesis (H₀)

There is no significant difference in the mean profit margins between top-performing and low-performing vendors.

### Alternative Hypothesis (H₁)

There is a significant difference in the mean profit margins between top-performing and low-performing vendors.

---

# Visualizations

The project includes:

- Count Plots
- Correlation Heatmap
- Scatter Plot
- Horizontal Bar Charts
- Pareto Chart
- Donut Chart
- Box Plot
- Histograms with Confidence Intervals

---

# Dashboard

The final dashboard summarizes key business metrics including:

- Total Sales
- Total Purchase
- Gross Profit
- Profit Margin
- Unsold Capital
- Purchase Contribution
- Top Vendors
- Top Brands
- Vendor Distribution
- Brand Performance

Replace the image path below with your dashboard image.

```markdown
![Dashboard](images/dashboard.png)
```

---

# Key Business Questions Answered

✔ Which vendors generate the highest sales?

✔ Which brands contribute the most revenue?

✔ Which vendors account for the majority of procurement?

✔ Does bulk purchasing reduce unit purchase price?

✔ Which vendors have the highest capital locked in inventory?

✔ Which brands have high profit margins but low sales?

✔ Are the profit margins of top-performing vendors statistically different from low-performing vendors?

---

# Repository Structure

```
Vendor-Performance-Analysis
│
├── Exploratory Data Analysis.ipynb
├── Vendor Performance Analysis.ipynb
├── get_vendor_summary.py
├── dashboard.png
├── requirements.txt
└── README.md
```

---

# Skills Demonstrated

- SQL Data Extraction
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis
- Business Analytics
- Procurement Analytics
- Inventory Analytics
- Statistical Analysis
- Hypothesis Testing
- Dashboard Development
- Business Storytelling

---

# Future Improvements

- Interactive Power BI Dashboard
- Streamlit Web Application
- Automated ETL Pipeline
- Sales Forecasting
- Vendor Segmentation
- Inventory Forecasting

---

## Author

**Pranay Shah**

If you found this project useful, consider giving it a ⭐.
