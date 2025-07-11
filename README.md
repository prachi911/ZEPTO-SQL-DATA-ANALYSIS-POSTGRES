# Zepto SQL Data Analysis (Postgres)

This project provides a comprehensive set of SQL queries and data cleaning scripts for analyzing product and inventory data in a PostgreSQL database, inspired by Zepto's data structure.

## Table Structure
The main table, `zepto`, contains the following columns:
- `sku_id`: Serial Primary Key
- `category`: Product category
- `name`: Product name
- `mrp`: Maximum Retail Price (in rupees)
- `discountPercent`: Discount percentage
- `availableQuantity`: Quantity available in stock
- `discountedSellingPrice`: Price after discount (in rupees)
- `weightInGms`: Product weight in grams
- `outOfStock`: Boolean indicating stock status
- `quantity`: Quantity (purpose may overlap with `availableQuantity`)

## Features
- **Table Creation & Data Export**: Create the `zepto` table and export data.
- **Data Exploration**: Count records, view all data, and check for null values.
- **Category Analysis**: List unique product categories.
- **Stock Analysis**: Compare out-of-stock vs. in-stock products.
- **Duplicate Detection**: Find products with the same name listed multiple times.
- **Data Cleaning**:
  - Identify and remove products with `mrp = 0`.
  - Convert prices from paise to rupees.
- **Data Analysis**:
  - Top 10 best-value products by discount percentage.
  - High MRP products that are out of stock.
  - Estimated revenue per category.
  - Products with MRP > ₹500 and discount < 10%.
  - Top 5 categories by average discount.
  - Price per gram for products above 100g.
  - Categorize products by weight (Low, Medium, Bulk).
  - Total inventory weight per category.

## Usage
1. **Import the SQL file** into your PostgreSQL database:
   ```sh
   psql -U <username> -d <database> -f zepto_sqldata_analyis.sql
   ```
2. **Modify or extend queries** as needed for your analysis.

## Requirements
- PostgreSQL database

