#Promo Sale Analysis

Overview

Company XYZ held a promo sale for their signature items (x, y, z). The goal is to analyze the sales data and create a marketing strategy to target age groups by looking at total quantities purchased. Specifically, we extract total quantities of each item bought per customer aged 18-35.

#Objectives

Extract the total quantities of each item bought per customer aged 18-35.

Sum each item per customer and exclude items with zero purchases.

Ensure there are no decimal values (company does not sell fractional items).

Provide two solutions: one using pure SQL and another using Pandas.

Store the extracted data into a CSV file using a semicolon (;) as the delimiter.

#Dataset

The project involves the following database tables:

customers - Contains customer details, including age.

items - Lists the items available for purchase.

sales - Records sales transactions.

orders - Contains details about each order, linking sales to items.

Approach

1. SQL Solution

Using a SQL query to join, filter customers aged 18-35, sum item quantities per customer, and exclude zero-quantity items:
sql_answer.sql file

2. Pandas Solution - sales_calculation.ipynb is the answer file

Merge customer, sales, orders, and items data.

Filter customers aged 18-35.

Group by customer_id, summing the quantity

Convert the quantity column to integers to remove decimal points.

Save the final dataset to a CSV file (quantity_by_customer_item.csv).

Group by customer_id and item_name, summing the quantity column from the filtered dataset.

Convert the quantity column to integers to remove decimal points.

Save the final dataset to a CSV file (quantity_by_customer.csv).

How to Run

Ensure Python (Pandas, SQLite3) is installed.
Load the dataset into an SQLite database.
Execute either the SQL query or Pandas script.
The final CSV file will be saved with a semicolon delimiter.

Notes
This script assumes all tables exist in S30_ETL_Assignment.db.

Ensure data integrity before running the queries.

Modify filters if age groups or item lists need changes.


Author: Marion Bill F. Garcia

Last Modified: 2025-03-05

