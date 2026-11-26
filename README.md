# Customer Behavior Analysis

An end-to-end customer shopping behavior analytics project using Python, SQL Server, and Power BI to explore customer purchasing patterns, preferences, and shopping habits.

## Project Overview

Understanding customer behavior is important for businesses to improve customer engagement, identify purchasing patterns, and make data-driven decisions.

This project analyzes a customer shopping dataset containing **3,900 records and 18 attributes**. It uses Python for data exploration and preprocessing, SQL Server for database querying, and Power BI for dashboard-based visualization.

## Tools & Technologies

- **Python:** Pandas, Jupyter Notebook
- **Database:** Microsoft SQL Server
- **Visualization:** Microsoft Power BI
- **Data Format:** CSV

## Dataset Description

The dataset contains 3,900 customer shopping records with information about:

- Customer demographics: Age, Gender, Location
- Product information: Item Purchased, Category, Size, Color, Season
- Purchase information: Purchase Amount, Previous Purchases, Frequency of Purchases
- Customer experience: Review Rating, Subscription Status
- Transaction details: Payment Method, Shipping Type, Discount Applied, Promo Code Used

## Project Workflow

### 1. Data Exploration

Used Python and Pandas to:
- Inspect the dataset using `head()` and `info()`.
- Generate descriptive statistics using `describe()`.
- Identify missing values.
- Examine the dataset structure and column distributions.

### 2. Data Cleaning and Preprocessing

Performed the following operations:

- Handled missing values in `Review Rating` using the median rating within each product category.
- Standardized column names by converting them to lowercase and replacing spaces with underscores.
- Renamed `purchase_amount_(usd)` to `purchase_amount`.
- Created customer age groups using quantile-based binning with `pd.qcut()`.
- Converted purchase frequency categories into approximate day intervals.
- Identified duplicate information between `discount_applied` and `promo_code_used` and removed the redundant column.

### 3. SQL Server

Used Microsoft SQL Server to work with the customer shopping dataset.

The repository includes a SQL script for selecting and accessing the customer shopping behavior table.

### 4. Power BI Dashboard

The repository includes a Power BI dashboard file (`customer_shopping_behavior.pbix`) for visual exploration of customer shopping data.

## Repository Structure

```text
Customer_Behavior_Analysis/
│
├── CSBA.ipynb
├── Customer_shopping_behaviorSQL.sql
├── customer_shopping_behavior.csv
├── customer_shopping_behavior.pbix
├── README.md
└── LICENSE
```

## How to Run the Project

### Step 1: Clone the repository

```bash
git clone https://github.com/SannihithRicky/Customer_Behavior_Analysis.git
```

### Step 2: Install dependencies

```bash
pip install pandas numpy jupyter
```

### Step 3: Open the Jupyter Notebook

```bash
jupyter notebook
```

Open `CSBA.ipynb` and load the dataset:

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

### Step 4: SQL Server

- Create or select the `customer_behavior` database.
- Import the CSV data into a table named `customer_shopping_behavior`.
- Execute the SQL script using SQL Server Management Studio.

### Step 5: Power BI

Open `customer_shopping_behavior.pbix` using Microsoft Power BI Desktop.

## Key Learning Outcomes

- Practical experience in data exploration and preprocessing.
- Handling missing values and redundant columns.
- Feature engineering using Pandas.
- Working with Microsoft SQL Server.
- Developing customer analytics workflows.
- Connecting data analysis with business intelligence visualization.

## Author

**Sannihith Yadav Gorla**

GitHub: https://github.com/SannihithRicky

---

If you find this project useful, feel free to explore the repository and share your feedback.

