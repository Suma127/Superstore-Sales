
# Superstore Sales Analysis using Databricks SQL

## Project Overview
This project focuses on analyzing retail sales data using Databricks SQL to identify business insights related to regional sales performance, product sales trends, and shipping efficiency.The dataset contains customer orders, product details, shipping information, and sales transactions.

---

## Tools Used
- Databricks
- SQL
- Excel/CSV Dataset
- GitHub

---

## Dataset Columns
- Order ID
- Order Date
- Ship Date
- Ship Mode
- Customer ID
- Customer Name
- Segment
- Country
- City
- State
- Postal Code
- Region
- Product ID
- Category
- Sub-Category
- Product Name
- Sales

---

## Data Cleaning Performed
- Removed duplicate records
- Verified data types
- Ensured Order Date and Ship Date were in proper date format
- Created derived columns:
  - Order Year
  - Order Month
  - Shipping Days

---

## SQL Analysis Performed

### Regional Sales Analysis
Identified highest and lowest performing sales regions.

**Insight:**
- West region generated highest sales (~710K)
- South region generated lowest sales (~389K)

---

### Monthly Sales Trend Analysis
Analyzed monthly sales performance to identify seasonality.

---

### Top Selling Products
Identified top-performing products based on sales revenue.

---

### Shipping Analysis
Calculated shipping duration using order date and ship date.

---
## Dashboard Screenshots
<img width="1223" height="440" alt="Top 10 Products by Sales" src="https://github.com/user-attachments/assets/c9765da4-115a-4d2e-8eff-9bb740418379" />
<img width="1223" height="440" alt="Monthly Sales Trend" src="https://github.com/user-attachments/assets/55f2ec94-f65c-4000-91f1-6fd1239c9aa8" />
<img width="606" height="257" alt="pie" src="https://github.com/user-attachments/assets/5721d0b7-effc-44a1-934e-d6e581c93969" />
<img width="710" height="440" alt="Sales by Category" src="https://github.com/user-attachments/assets/ff8d0cde-8bd6-4664-aeac-f7c477d90f81" />
<img width="606" height="290" alt="Sales by Segment" src="https://github.com/user-attachments/assets/521d0188-06eb-414b-a3b9-a750b06d3f4e" />

---





## Key Business Insights
- West and East regions contribute major share of revenue
- South region needs sales improvement strategies
- Certain products contribute significantly to overall revenue
- Shipping efficiency can impact customer satisfaction

---
## Recommendation
- Focus on improving sales strategy in South and Central regions 
- Investigate product preferences by region 
- Check whether shipping delays impact low-performing regions 
- Identify top-performing products in West/East and replicate strategy elsewhere
---
## SQL Sample Query

```sql
SELECT Region,
SUM(Sales) AS Total_Sales
FROM superstore_sales
GROUP BY Region
ORDER BY Total_Sales DESC;
