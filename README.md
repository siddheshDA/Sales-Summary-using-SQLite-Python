# 📊 Task 7 - Basic Sales Summary using SQLite & Python

## 📌 Objective
The goal of this task is to:
- Connect Python to a SQLite database.
- Run SQL queries to summarize sales data.
- Display results using Pandas in a clean tabular format.
- Visualize revenue per product using Matplotlib.

---

## 🛠 Tools & Libraries
- **Python 3**
- **SQLite3** – Database engine
- **Pandas** – Data handling & analysis
- **Matplotlib** – Data visualization

---

## 📂 Project Workflow
1. **Create Database & Table**
   - A SQLite database `sales_data.db` is created with a single table `sales`.
   
2. **Insert Sample Data**
   - Sample sales records are inserted for 3 products.

3. **Run SQL Query**
   - Calculate:
     - Total Quantity Sold
     - Total Revenue
   - Grouped by product.

4. **Load into Pandas**
   - Query results are imported into Pandas DataFrame.

5. **Visualize Data**
   - A bar chart shows revenue per product with labeled values for clarity.

---

## 🗒 SQL Query Used
```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
