# customer_behavior_analysis
## Overview
This project performs an end-to-end data analytics workflow on customer shopping behavior data. It covers data loading, exploratory data analysis (EDA), data cleaning, SQL querying, and interactive dashboard building in Power BI — designed to uncover actionable insights about customer purchasing patterns.

> **Goal:** Understand how customers shop, identify top-performing categories, and surface trends that support business decision-making.

---

## Repository Structure

```
customer_behavior_analysis/
│
├── Customer_Shopping_Behavior_Analysis.ipynb   # Main Jupyter Notebook (EDA + Cleaning)
├── customer_shopping_behavior.csv              # Raw dataset
├── customer_behavior_queries.sql               # SQL queries for analysis
├── customer_behavior_dashboard.pbix            # Power BI interactive dashboard
├── LICENSE
└── README.md
```

---

## Dataset

**File:** `customer_shopping_behavior.csv`

The dataset contains records of customer transactions and behavioral attributes including demographics, purchase history, preferences, and ratings.

| Column | Description |
|---|---|
| Customer ID | Unique identifier per customer |
| Age | Customer age |
| Gender | Male / Female |
| Item Purchased | Product name |
| Category | Product category (Clothing, Footwear, etc.) |
| Purchase Amount (USD) | Transaction value |
| Location | State / region of customer |
| Season | Season at time of purchase |
| Review Rating | Customer rating (1–5) |
| Subscription Status | Whether customer has a subscription |
| Payment Method | Mode of payment used |
| Frequency of Purchases | How often the customer shops |

> Source: [Kaggle — Customer Shopping Behavior Dataset](https://www.kaggle.com/)

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data loading, cleaning, manipulation |
| Matplotlib, Seaborn | Data visualization during EDA |
| Jupyter Notebook | Interactive analysis environment |
| SQL (PostgreSQL / MySQL) | Querying and aggregating structured data |
| Power BI Desktop | Interactive business dashboard |
| GitHub | Version control and project sharing |

---

## Project Steps

### 1. Data Loading
- Loaded `customer_shopping_behavior.csv` using `pandas.read_csv()`
- Inspected shape, column types, and sample records
- Identified missing values and duplicate rows

### 2. Exploratory Data Analysis (EDA)
- Summary statistics for numerical and categorical columns
- Distribution of age, purchase amount, and review ratings
- Purchase breakdown by category, season, gender, and location
- Correlation analysis between key variables

### 3. Data Cleaning
- Handled missing/null values
- Removed duplicate records
- Standardized data types and column formats
- Validated value ranges (e.g., ratings between 1–5)

### 4. SQL Queries
Queries written in `customer_behavior_queries.sql` include:
- Total revenue and average order value by category
- Top 10 customers by purchase amount
- Purchase trends by season and location
- Subscription vs. non-subscription spend comparison
- Payment method distribution analysis

### 5. Power BI Dashboard
Built in `customer_behavior_dashboard.pbix`:
- KPI cards: Total Revenue, Total Customers, Avg Purchase, Avg Rating
- Revenue by Category and Season (bar charts)
- Customer distribution by Gender and Location (map + donut)
- Subscription status impact on spend (clustered bar)
- Interactive slicers: Season, Category, Gender, Subscription Status

---

## Key Findings

- **Top category:** Clothing — accounts for the highest share of total purchases
- **Peak season:** Fall drives the most transactions across all categories
- **Payment preference:** Credit Card is the most commonly used payment method
- **Avg review rating:** ~3.7 out of 5 across all customers
- **Subscribers spend more:** Customers with active subscriptions show higher average order values

---

## How to Run

### Prerequisites
- Python 3.8+ with pip
- Jupyter Notebook or JupyterLab
- PostgreSQL / MySQL (optional, for SQL queries)
- Power BI Desktop (free download from Microsoft)

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/thanhbinhne/customer_behavior_analysis
cd customer_behavior_analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 3. Launch the notebook
jupyter notebook Customer_Shopping_Behavior_Analysis.ipynb
```

**For SQL analysis:**
```sql
-- Run queries in customer_behavior_queries.sql
-- using your preferred SQL client (pgAdmin, DBeaver, MySQL Workbench, etc.)
```

**For Power BI dashboard:**
```
1. Open Power BI Desktop
2. File → Open → customer_behavior_dashboard.pbix
3. Refresh data source if prompted
```

---

## Contact

**Thanh Binh** · [@thanhbinhne](https://github.com/thanhbinhne)
