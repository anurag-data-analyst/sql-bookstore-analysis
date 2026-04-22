# 📊 Online Bookstore Data Analysis (SQL)

## 📌 Overview
This project analyzes an online bookstore database using SQL to extract meaningful insights about sales, customers, and inventory.

## 🛠 Tools Used
- PostgreSQL
- SQL

## 📂 Dataset Tables
- Books
- Customers
- Orders

## 🔍 Key Analysis
- Total books sold by genre
- Average price analysis
- Top customers by spending
- Most sold books
- Order frequency analysis
- Stock remaining calculation

## 💡 Key Concepts Used
- JOIN
- GROUP BY
- HAVING
- ORDER BY
- LIMIT
- COALESCE
- Aggregate Functions

## 📈 Insights
- Identified top customers based on spending
- Found most popular book genres
- Analyzed sales trends and order patterns
- Calculated remaining stock after orders

## 📸 Sample Query
```sql
SELECT c.customer_id, c.name, SUM(o.total_amount) AS total_spent
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
GROUP BY c.customer_id, c.name
ORDER BY total_spent DESC
LIMIT 3;
