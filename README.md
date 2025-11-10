# 📊 Excel Sales Dashboard

## 🧩 Project Overview
An interactive **Excel Dashboard** built to analyze company sales performance — from **data cleaning in Power Query** to **analytical modeling using Pivot Tables and custom Measures**.  
The dashboard provides multi-dimensional insights on sales, profit, customers, and seasonal performance.

---

## 🧰 Tools & Techniques
- **Microsoft Excel**
  - Power Query for data transformation  
  - Pivot Tables for data modeling  
  - Pivot Charts for visualization  
  - Slicers for interactivity  
  - Calculated Measures (DAX-style formulas in Excel)  
  - Conditional Formatting for KPIs  

---

## 🧪 Data Processing Workflow

### 🔹 1. Data Cleaning (Power Query)
Performed using the **Power Query Editor**:
- Removed redundant and empty columns  
- Trimmed extra spaces in text fields  
- Converted column data types (text, date, decimal)  
- Reordered and renamed fields for consistency  
- Added calculated columns:
  - `Profit = Sales – Cost`
  - `Profit Margin % = (Profit / Sales) * 100`
  - `Season = based on MonthNumber (Winter, Spring, Summer, Autumn)`
- Grouped and summarized data by country and category to get **average order value** and **total sales per region**.

---

### 🔹 2. Data Modeling (Pivot Tables & Measures)

After cleaning, the dataset was loaded into **Excel Data Model** to build multiple **Pivot Tables** connected to slicers.

Created custom **measures** using calculated fields to ensure accurate and dynamic KPIs, including:

| Measure | Formula / Description |
|----------|-----------------------|
| **Total Sales** | `=SUM('Sales data'[Order_value_EUR_cleaned])` |
| **Total Cost** | `=SUM('Sales data'[Cost Cleaned])` |
| **Total Profit** | `=[Total Sales] - [Total Cost]` |
| **Profit Margin %** | `=[Total Profit] / [Total Sales]` |
| **Average Order Value** | `=[Total Sales] / DISTINCTCOUNT('Sales data'[Order_ID])` |
| **Sales per Customer** | `=[Total Sales] / DISTINCTCOUNT('Sales data'[Customer_Name])` |

These measures were applied across pivot tables for:
- **Sales by Country / Category / Device Type / Season**
- **Top 10 Customers**
- **Top Sales Managers and Representatives**
- **Year-over-Year (YoY) Sales Comparison**

---

## 📈 Dashboard Insights

### 🌍 **1. Geographical Insights**
- **Top Country:** Sweden generated the highest total sales and profit.  
- **High Performers:** France and Portugal followed closely.  
- **Average Order Value:** Highest in Sweden (€167K).

---

### 🏷️ **2. Product & Category Insights**
- **Most Profitable Category:** Clothing.  
- **Highest Profit Margins:**  
  - Outfits → **17.79%**  
  - Books → **16.59%**  
  - Other → **16.38%**.  
- Games and Accessories had relatively lower margins.

---

### 💻 **3. Device Type Insights**
- **PC** accounted for the majority of sales (≈ €89M).  
- Tablets and Mobiles contributed smaller shares.  
- Suggests desktop devices remain the dominant purchase channel.

---

### 👩‍💼 **4. Sales Team Performance**
- **Top Sales Manager:** Celine Tumaisan.  
- **Top Sales Rep:** “On the Stream” achieved the highest profit among all representatives.  
- Differences across managers reveal optimization opportunities.

---

### 📅 **5. Time & Season Insights**
- **Yearly Trend:** 2020 outperformed 2019 in both sales and profit.  
- **Seasonal Pattern:**  
  - Summer led with 27% of total sales.  
  - Winter recorded slightly lower results.  
- Monthly data shows upward sales trend toward Q3.

---

## 📊 Key Performance Metrics

| Metric | Value |
|:--|--:|
| **Total Sales** | €113,335,099.10 |
| **Total Cost** | €94,470,064.60 |
| **Total Profit** | €18,865,034.51 |
| **Profit Margin %** | 16.65% |
| **Orders Count** | 1001 |
| **Average Order Value** | €113,221.90 |
| **Total Customers** | 75 |
| **Sales per Customer** | €1,511,134.70 |

---

## 📸 Dashboard Preview
<p align="center">
  <img src="Sales%20Project.xlsx%20-%20Excel%2011_10_2025%205_42_25%20PM.png" alt="Sales Dashboard" width="900"/>
</p>

---

## 🚀 How to Use
1. Open `Sales Project.xlsx` in Excel.  
2. Go to the **Dashboard** sheet to view visuals.  
3. Use **Slicers** to filter by:
   - Year / Month  
   - Device Type  
   - Country / Category / Sales Manager  
4. Explore **Pivot Tables** for detailed breakdowns.

---

## 👨‍💻 Author
**Mostafa Elrkhawy**  
Excel & BI Analyst  
📧 [https://www.linkedin.com/in/mostafa-elrkhawy/]  
📅 Project Type: Excel Dashboard & Business Intelligence
