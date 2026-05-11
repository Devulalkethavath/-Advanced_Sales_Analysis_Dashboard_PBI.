# 📊 Advance Sales Analysis Dashboard PBI

## 📌 Project Overview

This repository showcases a comprehensive **Advance Sales Analysis Dashboard** developed using Microsoft Power BI to provide actionable insights into sales performance, profitability, customer trends, and regional analysis across the USA.

The dashboard enables users to dynamically analyze sales data using interactive filters and visualizations, helping businesses identify high-performing areas, sales trends, and operational opportunities for better decision-making.

📂 Download the `.pbix` file and open it using Microsoft Power BI Desktop.

### 📁 Project File

---

# 🚀 Key Features & Insights

The dashboard is designed with multiple interactive report views to provide deep business insights and performance tracking.

---

# 📊 Report Snapshot (Power BI Desktop)

### 1️⃣ Executive Sales Performance Overview

This report provides a high-level summary of overall business performance.

### Key Metrics Included:
- Total Sales
- Total Profit
- Total Orders
- Sales Growth %
- Profit Margin

### Visual Insights:
- Monthly Revenue Trends
- Year-over-Year Sales Comparison
- Sales by Region
- Top Performing Categories
- KPI Performance Indicators

---

### 2️⃣ Regional Sales Analysis

Analyze sales performance across different states and cities.

### Insights:
- Top Revenue Generating States
- City-wise Sales Distribution
- Regional Profitability Trends
- Geographic Sales Patterns

---

### 3️⃣ Product & Category Analysis

Track category and sub-category performance.

### Includes:
- Best Selling Products
- Top Performing Categories
- Profit Contribution by Category
- Sales Distribution Analysis

---

### 4️⃣ Customer & Salesperson Insights

Evaluate customer behavior and salesperson performance.

### Insights:
- Salesperson Contribution
- Customer Purchase Trends
- Sales Distribution by Segment
- Order Volume Analysis

---

### 5️⃣ Shipping & Order Analysis

Analyze operational performance through shipping insights.

### Includes:
- Ship Mode Performance
- Order Status Tracking
- Delivery Trends
- Shipping Efficiency Analysis

---

# 🎛 Dynamic Filtering Features

The dashboard supports interactive slicers and filters for detailed business analysis.

| Filter Dimension | Purpose |
|---|---|
| Year | Compare yearly performance |
| Month | Analyze monthly trends |
| Category | Focus on specific product groups |
| Region | Regional sales analysis |
| State | State-wise performance |
| Salesperson | Evaluate employee performance |
| Ship Mode | Shipping performance analysis |

---

# 🧩 DAX Queries Used

## Total Sales
```DAX
Total Sales =
SUM('Orders'[Sales])
```

## Total Profit
```DAX
Total Profit =
SUM('Orders'[Profit])
```

## Total Orders
```DAX
Total Orders =
DISTINCTCOUNT('Orders'[Order ID])
```

## Sales LY
```DAX
Sales LY =
CALCULATE(
    SUM('Orders'[Sales]),
    SAMEPERIODLASTYEAR(DateTable[Date])
)
```

## Sales YoY %
```DAX
Sales YoY % =
DIVIDE(
    [Total Sales] - [Sales LY],
    [Sales LY],
    0
)
```

## Profit Margin
```DAX
Profit Margin =
DIVIDE([Total Profit],[Total Sales],0)
```

## Calendar Table
```DAX
Calendar_Table =
ADDCOLUMNS(
    CALENDAR(DATE(2014,1,1), DATE(2016,12,31)),
    "Year", YEAR([Date]),
    "Month Number", MONTH([Date]),
    "Month Name", FORMAT([Date], "MMMM"),
    "Month Short", FORMAT([Date], "MMM"),
    "MonthYear", FORMAT([Date], "MMM-YYYY"),
    "Quarter", "Q" & FORMAT([Date], "Q")
)
```

---

# 🛠 Technologies Used

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Interactive Data Visualization
- Business Intelligence Techniques

---

# 📈 Dashboard Capabilities

✅ Sales Trend Analysis  
✅ KPI Monitoring  
✅ Regional Insights  
✅ Product Performance Tracking  
✅ Dynamic Filtering  
✅ Interactive Drill-Down Analysis  
✅ Profitability Analysis  
✅ Customer Insights  

---

# 🎯 Business Impact

This dashboard helps organizations:

- Monitor sales performance effectively
- Identify profitable regions and categories
- Improve operational decision-making
- Track business growth trends
- Enhance sales strategy planning

---

# 📷 Dashboard Snapshots

👉 Add your dashboard screenshots here.

---

# 👨‍💻 Author

### Dashboard Created By:
**Devulal Kethavath**

### Project Name:
**Advance_Sales_Analysis_Dashboard_PBI**

---

# 🎥 Interactive Dashboard Demo

👉 Add your LinkedIn demo video link here.

Example:
[Watch Dashboard Demo on LinkedIn](Your_Link_Here)

---

# 🔗 Connect With Me

## LinkedIn
Add Your LinkedIn Profile Link

## GitHub
Add Your GitHub Profile Link

---

# ⭐ Conclusion

The **Advance Sales Analysis Dashboard PBI** provides a powerful and interactive business intelligence solution for analyzing sales, profitability, customer trends, and operational performance.

This project demonstrates strong skills in Power BI, DAX, data visualization, and business analytics, helping businesses make data-driven decisions effectively.
