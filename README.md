# ☕ Coffee Shop Sales Analysis Dashboard

An Excel-based sales analytics dashboard built with Power Query, PivotTables, and interactive charts to uncover actionable insights into coffee shop performance across time, location, and product category.

---

## 📌 Problem Statement

The main objective of this project is to analyze retail sales data to gain actionable insights that will enhance the performance of the coffee shop — *"Start Your Day With Coffee."*

## 🎯 Recommended Analysis

1. How do sales vary by day of the week and hour of the day?
2. Are there any peak times for sales activity?
3. What is the total sales revenue for each month?
4. How do sales vary across different store locations?
5. What is the average price per order and per person?
6. Which products are the best-selling in terms of quantity and revenue?
7. How do sales vary by product category and type?

## 🛠️ Steps Performed

1. **ETL (Extract – Transform – Load)** using Power Query
   - Imported raw transaction data into Power Query
   - Cleaned and preprocessed the data (handled data types, added calculated columns)
   - Closed and loaded the data into Excel, then added it to the Data Model
2. **Created PivotTables and Measures** to summarize sales, quantity, and order metrics
3. **Built Charts** to visualize trends across time, product, and location
4. **Assembled the Dashboard** — added charts, KPI cards, titles, and slicers
5. **Finalized dashboard design** for a clean, decision-ready view

---

## 🗂️ Dataset

**Sheet:** `Transactions`
**Size:** ~149,116 transaction records

| Column | Description |
|---|---|
| `transaction_id` | Unique identifier for each transaction |
| `transaction_date` | Date of the transaction |
| `transaction_time` | Time of the transaction |
| `transaction_qty` | Quantity of items purchased |
| `store_id` | Store identifier |
| `store_location` | Store location (Astoria, Hell's Kitchen, Lower Manhattan) |
| `product_id` | Product identifier |
| `unit_price` | Price per unit |
| `product_category` | Product category (Coffee, Tea, Bakery, Branded, Coffee beans, Drinking Chocolate, Flavours, Loose Tea, Packaged Chocolate) |
| `product_type` | Product type/sub-category |
| `product_detail` | Specific product name/description |
| `Day Name` | *Calculated:* day of the week the transaction occurred |
| `Hour` | *Calculated:* hour of the day the transaction occurred |
| `Month Name` | *Calculated:* month of the transaction |
| `total Bill` | *Calculated:* `transaction_qty × unit_price` |
| `Order size` | *Calculated:* order size bucket (Small, Regular, Large, Not Defined) |

---

## 📊 Workbook Structure

The workbook contains **3 sheets**:

### 1. `Transactions`
Raw and cleaned transaction-level data, enriched with calculated columns (Day Name, Hour, Month Name, Total Bill, Order Size) built via Power Query, and loaded into the Excel Data Model.

### 2. `Pivot tables`
Supporting PivotTables that power the dashboard visuals:
- Sales by day of the week
- Sales revenue by month
- Sales by hour of the day (by transaction quantity)
- Sales by category
- Sales by location
- Sales by order size
- Top 5 products by sales

### 3. `Dashboard`
The final interactive dashboard, featuring:
- **KPI cards:** Total Revenue Generated, Total Footfall, Average Bill/Order, Average Bill/Person
- **Charts:**
  - Categorywise Sales
  - Monthly Sales
  - Sales by Location
  - Quantity Ordered based on Hours
  - Sales on Weekdays
  - Top 5 Products based on Sales
  - % Distribution of Sales (by category / order size)
  - Sizewise Order distribution
- **Slicers** for interactive filtering (e.g., by location, product category)

---

## 📈 Key KPIs

- **Total Revenue Generated:** ₹6,98,812.33
- **Total Footfall:** 149,116 transactions
- **Average Bill / Order:** 4.69
- **Average Bill / Person:** 1.44

## 💡 Sample Insights

- **Coffee** is the top-selling category by revenue, followed by **Tea** and **Bakery**
- **Barista Espresso** ranks among the top-selling individual products
- Sales activity is fairly evenly split across the three store locations (Astoria, Hell's Kitchen, Lower Manhattan)
- **Large**-sized orders generate the highest revenue among order-size buckets, followed by orders with an undefined size
- Sales volume builds through the morning hours and peaks around mid-morning to early afternoon (8 AM–11 AM), tapering off later in the day

---

## 🛠️ Tools Used

- **Microsoft Excel** — Power Query (ETL), PivotTables, PivotCharts, Data Model, Slicers
- **Source data:** Raw coffee shop transaction records

## 📁 Repository Structure

```
├── README.md
└── Coffee_Shop_Sales.xlsx     # Excel workbook (Transactions, Pivot tables, Dashboard)
```

## ▶️ How to Use

1. Open `Coffee_Shop_Sales.xlsx` in Microsoft Excel (Power Query and Data Model features require Excel 2016+ or Microsoft 365).
2. Go to the **Dashboard** sheet to view KPIs and charts.
3. Use the **slicers** to filter the dashboard by store location, product category, or other dimensions.
4. To refresh the underlying data: go to the **Transactions** sheet, update/replace the source data, then use **Data → Refresh All** to update the Power Query transformations, PivotTables, and Dashboard.

## 🎯 Project Outcome

This project demonstrates an end-to-end Excel analytics workflow — extracting and cleaning transactional data with Power Query, modeling it for analysis, and presenting the results through an interactive, slicer-driven dashboard that surfaces sales trends by time, location, product, and order size to support coffee shop performance decisions.
