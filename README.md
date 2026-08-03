# Zepto SQL Analysis

A SQL project analyzing Zepto's (quick-commerce) product catalog — covering data exploration, data cleaning, and 8 business questions using PostgreSQL.

## 📌 Overview
This project simulates a real-world scenario: cleaning messy e-commerce product data and answering business questions that a category or operations team might actually ask — around pricing, discounts, stock, and inventory.

## 🗂️ Dataset
The `zepto` table includes the following columns:
| Column | Description |
|---|---|
| `sku_id` | Unique product identifier |
| `category` | Product category |
| `name` | Product name |
| `mrp` | Maximum Retail Price |
| `discountPercent` | Discount offered on MRP |
| `availableQuantity` | Units available |
| `discountedSellingPrice` | Final selling price after discount |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Stock status (true/false) |
| `quantity` | Order quantity |

## 🧹 Data Cleaning Steps
- Checked for `NULL` values across all key columns
- Removed rows where `mrp = 0` (invalid/incomplete listings)
- Converted `mrp` and `discountedSellingPrice` from paise to rupees

## ❓ Business Questions Answered
1. Top 10 best-value products based on discount percentage
2. Products with high MRP that are out of stock
3. Estimated revenue per category
4. Products with MRP > ₹500 and discount < 10%
5. Top 5 categories with the highest average discount
6. Price-per-gram for products above 100g (best value)
7. Weight-based product segmentation (Low / Medium / Bulk)
8. Total inventory weight per category

## 🛠️ Tools Used
- PostgreSQL
- SQL (joins, aggregations, `CASE` statements, grouping, filtering)

## 🚀 How to Run
1. Create a PostgreSQL database.
2. Run `zepto_sql_analysis.sql` in your SQL client (pgAdmin, DBeaver, or `psql`) — it creates the table and runs all the analysis queries.
3. Load your own Zepto dataset CSV into the `zepto` table before running the exploration/cleaning/business-question sections.

## 👤 Author
Shalini Radhakrishnan

