<img width="1367" height="827" alt="dashboard_screenshot png" src="https://github.com/user-attachments/assets/0bc7c154-6869-4888-8c8b-d37a799be311" />
# Retail Sales Performance Dashboard 📊

An advanced, end-to-end **Power BI Dashboard** developed to analyze retail store performance, product sales trends, and business efficiency. This project transforms raw retail transaction data into actionable business insights for stakeholders.

---



---

## 🚀 Key Features & Insights
* **Executive Performance Window:** Analyzes key business metrics including Total Revenue ($2M), Total Units Sold (25K), and Net Transactions.
* **Time-Intelligence Analysis:** Tracks **Month-over-Month (MoM) Growth (35%)** using advanced DAX parameters to compare current performance against historical data.
* **Geographical Distribution:** Visualizes retail store performance using a custom geographic bubble map mapped via **Latitude & Longitude** variables.
* **Product Optimization:** Ranks the **Top 5 & Bottom 5 Products** by revenue to quickly identify star products and underperforming inventory.
* **Return Rate Analysis:** Features a **Product Return Rate Breakdown (37% overall)** by category to help mitigate logistics issues.

---

## 🛠️ Data Architecture & DAX Measures Used
The data model follows a robust **Star Schema** linking Fact and Dimension tables. Key DAX formulas implemented include:

### 1. Total Revenue
```dax
Total Revenue = SUM('Sales'[Amount])
```

### 2. Month-over-Month (MoM) Sales Growth %
```dax
Sales MoM % = 
VAR SalesLM = CALCULATE([Total Revenue], DATEADD('Calendar'[Date], -1, MONTH))
RETURN DIVIDE([Total Revenue] - SalesLM, SalesLM, 0)
```

### 3. Product Return Rate %
```dax
Return Rate % = DIVIDE(SUM('Sales'[Returns \$]), [Total Revenue], 0)
```

---

## 🛠️ Tech Stack & Tools
* **Power BI Desktop** (Data Visualization & Modeling)
* **Power Query Editor** (ETL - Data Transformation)
* **DAX** (Data Analysis Expressions for Calculated Measures)

---

## 📂 Project Structure
* `Retail_Sales_Performance_Dashboard.pbix` - Core Power BI project file.
* `dashboard_screenshot.png` - Visual preview of the dashboard interface.
