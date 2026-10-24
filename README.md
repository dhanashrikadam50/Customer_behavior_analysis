# Customer Shopping Behavior Analysis

## Overview

This project analyzes customer shopping behavior to identify purchasing patterns, customer preferences, product performance, and key business insights.

The project follows an end-to-end data analytics workflow, starting with data loading and cleaning in Python, followed by exploratory data analysis, SQL analysis using SQL Server, and interactive dashboard creation in Power BI.

### Project Workflow

**Dataset → Python → Data Cleaning & EDA → SQL Server → SQL Analysis → Power BI Dashboard → Business Report**

---

## Dataset

The project uses a **Customer Shopping Behavior** dataset containing customer and transaction-related information.

### Key Data Fields

- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Discount Applied
- Previous Purchases
- Payment Method
- Frequency of Purchases

The dataset was prepared and cleaned before performing further analysis.

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** | Data loading, cleaning and EDA |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical operations |
| **Matplotlib / Seaborn** | Data visualization during EDA |
| **SQL Server** | Data storage and SQL analysis |
| **SQL** | Business queries and KPI analysis |
| **Power BI** | Interactive dashboard |
| **Excel / CSV** | Initial dataset format |
| **Git & GitHub** | Project version control |

---

## Project Steps

### 1. Load Dataset

The dataset was loaded into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

Initial data inspection was performed using functions such as:

```python
df.head()
df.info()
df.describe()
df.isnull().sum()
```

---

### 2. Data Cleaning

The dataset was checked and prepared for analysis.

Key activities included:

- Handling missing values
- Removing duplicate records
- Correcting data types
- Standardizing text values
- Checking inconsistent values
- Handling missing review ratings
- Preparing the dataset for SQL analysis

Example:

```python
df["Review Rating"] = df.groupby("Category")["Review Rating"].transform(
    lambda x: x.fillna(x.median())
)
```

---

### 3. Exploratory Data Analysis (EDA)

EDA was performed to understand customer behavior and identify important patterns.

The analysis included:

- Customer demographics
- Product category performance
- Average purchase amount
- Review ratings
- Purchase frequency
- Subscription behavior
- Discount usage
- Payment methods
- Seasonal purchasing patterns
- Customer purchasing trends

Visualizations were created to identify trends and relationships in the data.

---

### 4. Load Data into SQL Server

After cleaning, the prepared dataset was loaded into **Microsoft SQL Server**.

SQL Server was used to store the cleaned data and perform structured business analysis.

---

### 5. SQL Analysis

SQL queries were written to answer business questions and calculate important metrics.

Examples of analysis:

- Top-selling products
- Highest-rated products
- Average purchase amount by category
- Customer distribution by location
- Purchase behavior by gender
- Subscription vs. non-subscription customers
- Discount usage analysis
- Seasonal purchasing trends
- Customer purchase frequency
- Category-wise performance

Example query:

```sql
SELECT
    Category,
    ROUND(AVG(Purchase_Amount), 2) AS Average_Purchase
FROM customer_shopping_behavior
GROUP BY Category
ORDER BY Average_Purchase DESC;
```

---

## Power BI Dashboard

An interactive Power BI dashboard was created to present the key findings in an easy-to-understand format.

### Dashboard Includes

- Total Customers
- Total Purchases
- Total Purchase Amount
- Average Purchase Amount
- Average Review Rating
- Category-wise sales
- Customer demographics
- Purchase frequency
- Subscription analysis
- Payment method analysis
- Seasonal trends
- Product performance

The dashboard allows users to filter and explore customer behavior interactively.

---

## Results & Key Insights

The analysis provides insights into:

- Customer purchasing patterns
- Best-performing product categories
- Products with higher customer ratings
- Customer preferences based on demographics
- Impact of discounts on purchasing behavior
- Subscription customer behavior
- Popular payment methods
- Seasonal purchasing trends
- Purchase frequency patterns

These insights can help businesses improve **customer targeting, product strategy, promotions, and sales decisions**.

---

## Business Recommendations

Based on the analysis, businesses can:

- Focus on high-performing product categories.
- Improve marketing strategies for specific customer segments.
- Use customer ratings to identify product opportunities.
- Develop targeted offers for different customer groups.
- Analyze subscription behavior to improve customer retention.
- Optimize promotional and discount strategies.
- Use seasonal trends for better inventory and marketing planning.

---

## Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── python/
│   └── customer_behavior_analysis.py
│
├── sql/
│   └── customer_behavior_analysis.sql
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── report/
│   └── customer_behavior_analysis_report.pdf
│
└── README.md
```

---

## How to Run

### Step 1: Clone the Repository

```bash
git clone <your-github-repository-url>
```

### Step 2: Install Python Libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy
```

### Step 3: Load the Dataset

Place the CSV file inside the `data` folder.

### Step 4: Run Python Analysis

Open the Python file and run the data loading, cleaning, and EDA steps.

### Step 5: Load Data into SQL Server

Import the cleaned dataset into SQL Server and execute the SQL queries provided in the `sql` folder.

### Step 6: Open Power BI Dashboard

Open the `.pbix` file in Power BI Desktop and connect it to the SQL Server data if required.

### Step 7: Review the Report

The project report contains the methodology, analysis, findings, and business recommendations.

---

## Skills Demonstrated

**Data Analytics | Python | Pandas | SQL | SQL Server | EDA | Data Cleaning | Data Visualization | Power BI | Business Intelligence | KPI Analysis | Business Insights | Reporting**

---

## Author

**Dhanashri Kadam**

MBA – Business Analytics

Aspiring Data Analyst / Business Analyst.
