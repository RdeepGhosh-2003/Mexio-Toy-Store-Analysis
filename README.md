# 🎯 Mexico Toy Store Analytics Dashboard

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/Language-DAX-blue)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Retail%20Analytics-orange)
![Made by Raj](https://img.shields.io/badge/Author-Raj-blueviolet)

---

> 🚀 End-to-end Power BI project delivering actionable insights across **Sales, Inventory, Products, and Store Performance**

---

## 🧠 Project Overview

This project analyzes a multi-store toy retail business using Power BI and transforms raw data into a **decision-making dashboard**.

It answers key business questions:

- Which products drive revenue?
- Are we overstocked or at risk of stock-outs?
- Which stores and cities perform best?
- Where should the business focus?

---

## ⚡ Key Highlights

- 📊 4-page interactive dashboard  
- 🧱 Star schema data model  
- 🧮 Advanced DAX measures  
- 📦 Inventory risk analysis (low stock detection)  
- 📍 Store & regional performance insights  
- 🎨 Clean, consistent UI design  

---

## 🖼️ Dashboard Preview

### 🟢 Executive Overview
![Overview](<img width="659" height="376" alt="OVERVIEW" src="https://github.com/user-attachments/assets/ecb30911-563b-45a2-ab50-5baab7181789" />
)

### 🟠 Inventory Intelligence
![Inventory](<img width="660" height="372" alt="INVENTORY INTELLIGENCE" src="https://github.com/user-attachments/assets/500c4f09-7ef0-444d-98a4-5e975e2b227c" />
)

### 🔵 Product Analysis
![Product](<img width="659" height="374" alt="PRODUCT ANALYSIS" src="https://github.com/user-attachments/assets/e0ad6e53-5f07-4ce8-9112-c987c3d55304" />
)

### 🔴 Store Performance
![Store](<img width="659" height="373" alt="STORE PERFORMANCE" src="https://github.com/user-attachments/assets/460cf8ab-816e-45bd-9aa4-5b9bafda5ce6" />
)

---

## 🧱 Data Model

products  
   ↓  
sales ← calendar  
   ↑  
stores  
   ↑  
inventory  

---

## 📊 Dashboard Breakdown

### 🟢 Executive Overview
- KPI Cards: Total Sales, Profit, Quantity, Profit Margin  
- Sales trend over time  
- Top-performing stores  
- Sales by category  

👉 Provides a quick snapshot of overall business performance

---

### 🟠 Inventory Intelligence
- Stock vs Sales comparison  
- Low stock alerts 🚨  
- Inventory turnover  
- Stock distribution by category  

👉 Helps identify stock risks and optimize inventory

---

### 🔵 Product Analysis
- Top 10 products by sales  
- Category-wise sales & profit  
- Contribution % analysis  
- Product-level KPIs  

👉 Identifies key revenue drivers

---

### 🔴 Store Performance
- Store ranking by sales  
- Sales by city  
- Geographic visualization  
- Store-level KPIs  

👉 Evaluates regional and store performance

---

## 🧮 Key DAX Measures

Total Sales = SUMX(sales, sales[Units] * RELATED(products[Product_Price]))

Total Profit =
SUMX(
    sales,
    sales[Units] * 
    (RELATED(products[Product_Price]) - RELATED(products[Product_Cost]))
)

Stock Quantity = SUM(inventory[Stock_On_Hand])

Low Stock =
IF([Stock Quantity] < 500, 1, 0)

Contribution % =
DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(products)))

---

## 📈 Key Insights

- 🧸 Revenue is concentrated in top-performing products (e.g., Lego Bricks)  
- 📦 No dead stock observed → efficient inventory management  
- ⚠️ Multiple products are at risk of stock-out  
- 🏙️ Sales are concentrated in major cities like Ciudad de Mexico  
- 🏪 A few stores contribute significantly to total revenue  

---

## 🛠️ Tech Stack

- Power BI  
- DAX (Data Analysis Expressions)  
- Power Query  
- Excel  

---

## 💡 Business Value

This dashboard enables:

- 📦 Better inventory planning  
- 📊 Identification of high-performing products  
- 📍 Regional sales optimization  
- 🎯 Data-driven decision making  

---

## 🚀 How to Use

1. Download the `.pbix` file  
2. Open in Power BI Desktop  
3. Use slicers (Date, Store, Category) to interact  

---

## 🔮 Future Improvements

- Drill-through analysis pages  
- Forecasting (time series analysis)  
- Automated data refresh  
- Advanced tooltip insights  

---

## 👨‍💻 Author

**Raj**

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐
