Task 7 – SQLite + Python + Matplotlib
Overview
This task demonstrates how to:

Create and populate a SQLite database using Python.

Query and aggregate sales data with SQL.

Visualize the results using Matplotlib.

Steps Performed
1. Database Creation
Used the sqlite3 library to create a local SQLite database file (sales_data.db).

Created a sales table with columns:

product (TEXT)

quantity (INTEGER)

price (REAL)

2. Data Insertion
Inserted sample sales data:

Product	Quantity	Price
Laptop	5	50000
Mobile	10	15000
Tablet	7	20000
Headphones	15	2000
Charger	20	500

3. Data Querying
Used SQL aggregation to compute:

total_qty: total quantity sold for each product

revenue: total revenue (quantity × price)

sql
Copy
Edit
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
4. Visualization
Plotted a bar chart showing revenue per product using Matplotlib:

X-axis: Product names

Y-axis: Revenue in INR

Color: Sky Blue

Requirements
Install required packages before running:

bash
Copy
Edit
pip install pandas matplotlib
How to Run
Ensure Python is installed.

Save the .ipynb file and run it in Jupyter Notebook or VS Code.

The database will be created in the same folder as the script.

Output:

Console print of aggregated sales data.

Bar chart visualization.
