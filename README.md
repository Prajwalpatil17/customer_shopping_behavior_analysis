# customer_behavior_analysis
End-to-end analysis of retail customer shopping behavior using Python, SQL, and Power BI — from data cleaning to an interactive dashboard.
# Customer Shopping Behavior Analysis

An end-to-end data analytics project that analyzes retail customer shopping behavior to help a company improve sales, customer engagement, and marketing strategy. The project covers the full pipeline: data cleaning in Python, business analysis in SQL, and an interactive dashboard in Power BI.

## 📌 Business Problem

A retail company wants to understand its customers' shopping behavior to improve sales, satisfaction, and long-term loyalty. Management has noticed shifting purchase patterns across demographics, product categories, and sales channels, and wants to know which factors — discounts, reviews, seasons, payment methods — drive purchase decisions and repeat business.

**Business question:** *How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?*

## 📊 Dataset

- **Rows:** 3,900 transactions
- **Columns:** 18
- **Key fields:**
  - Customer demographics — Age, Gender, Location, Subscription Status
  - Purchase details — Item Purchased, Category, Purchase Amount, Season, Size, Color
  - Shopping behavior — Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type, Payment Method
- **Data quality:** 37 missing values in the Review Rating column

## 🛠️ Tools & Tech Stack

| Stage | Tool |
|---|---|
| Data cleaning & preparation | Python (Pandas) |
| Structured analysis | SQL (MySQL) |
| Visualization & dashboard | Power BI |
| Version control | Git / GitHub |

## 🔄 Project Workflow

### 1. Data Preparation (Python)
- Loaded the dataset with Pandas; explored structure with `df.info()` and `df.describe()`
- Handled missing values — imputed Review Rating nulls using the median rating per product category
- Standardized column names to snake_case
- Engineered new features: `age_group` (binned ages), `purchase_frequency_days`
- Checked for redundancy between `discount_applied` and `promo_code_used`; dropped `promo_code_used`
- Loaded the cleaned dataset into MySQL for SQL analysis

### 2. Data Analysis (SQL)
Ran structured queries in MySQL to answer key business questions, including:
1. Revenue by gender
2. High-spending customers who still used discounts
3. Top 5 products by average review rating
4. Purchase amount comparison — Standard vs. Express shipping
5. Subscribers vs. non-subscribers — spend and revenue
6. Products most dependent on discounts
7. Customer segmentation — New, Returning, Loyal
8. Top 3 products per category
9. Relationship between repeat purchases (>5) and subscription status
10. Revenue contribution by age group

### 3. Visualization (Power BI)
Built an interactive **Customer Behavior Dashboard** featuring:
- KPI cards — number of customers, average purchase amount, average review rating
- Subscription status breakdown (donut chart)
- Revenue and sales by category
- Revenue and sales by age group
- Slicers for Subscription Status, Gender, Category, and Shipping Type

## 🔍 Key Insights

- Male customers generated significantly higher total revenue than female customers.
- Discount-driven purchases are common, but a meaningful segment of customers spend above average even while using discounts.
- Gloves, Sandals, and Boots have the highest average review ratings.
- Express shipping customers spend marginally more on average than Standard shipping customers.
- The vast majority of customers (2,847 of 3,900) are non-subscribers, yet they contribute the bulk of total revenue.
- Hats, Sneakers, and Coats are the most discount-dependent products.
- Most customers fall into the "Loyal" segment (3,116), with far fewer New (83) or Returning (701) customers.
- Young Adults contribute the highest total revenue among age groups, closely followed by Middle-aged and Adult segments.

## 💡 Business Recommendations

- **Boost Subscriptions** — Promote exclusive benefits to convert non-subscribers, who make up the largest customer base.
- **Customer Loyalty Programs** — Reward repeat buyers to move more customers into the Loyal segment.
- **Review Discount Policy** — Balance discount-driven sales boosts against margin impact, especially for high-discount-dependent products.
- **Product Positioning** — Feature top-rated and best-selling products more prominently in marketing campaigns.
- **Targeted Marketing** — Focus campaigns on high-revenue age groups and express-shipping users.

## 📁 Repository Structure

```
customer-shopping-behavior-analysis/
├── python/
│   └── data_cleaning_eda.ipynb        # Data cleaning, EDA, feature engineering
├── sql/
│   └── business_queries.sql           # 10 business-question SQL queries
├── powerbi/
│   └── customer_behavior_dashboard.pbix
├── report/
│   └── Customer_Shopping_Behavior_Analysis.pdf
├── presentation/
│   └── Customer_Shopping_Behavior_Analysis.pptx
└── README.md
```

## 🚀 How to Reproduce

1. Clone the repository
2. Install dependencies: `pip install pandas`
3. Run the Python notebook to clean the raw data and generate `cleaned_data.csv`
4. Load the cleaned data into MySQL and run the queries in `sql/business_queries.sql`
5. Open `powerbi/customer_behavior_dashboard.pbix` in Power BI Desktop to explore the dashboard

## 👤 Author

**Prajwal Patil**
Data Analyst | Power BI • SQL • Python • Excel
GitHub: [Prajwalpatil17](https://github.com/Prajwalpatil17)
LinkedIn: [Prajwal Patil](https://www.linkedin.com/in/prajwalpatil17/)
