# 📊 Power BI Sales & Inventory Dashboard

![Dashboard Preview](screenshots/dashboard_overview.png)  
*A data-driven solution for tracking sales performance and inventory trends*

## 📌 Overview
This Power BI dashboard analyzes fruit and vegetable sales data to provide actionable business insights. The project was developed based on the [Sales and Inventory Analysis PDF](data/Sales_and_Inventory_Analysis.pdf) requirements.

## 📂 Dataset Structure
### Primary Tables:
1. **Sales** (357 transactions)
   - `FK_Customer`, `FK_Product`, `Quantity`, `UnitPrice`, `Discount`, `TotalAmount`
   
2. **Products** (25 items)
   - `PK_Product`, `ProductName`, `ProductCategory` (Fruit/Vegetable), `UnitPrice`
   
3. **Customers** (12 records)
   - Demographic data including `Gender`, `Country`, `Birthdate`

### Key Metrics Tracked:
- Total Sales: $1,247.82
- Total Quantity Sold: 642 units
- Average Discount: 8.2%

## 🎯 Dashboard Features
### 1. Customer Purchase Analysis
![Customer Analysis](screenshots/customer_purchase.png)
- Identifies top buyers by quantity purchased
- Gender distribution visualization (Male: 45%, Female: 55%)
- Country-based performance (France: 32%, Belgium: 41%, Netherlands: 27%)

### 2. Product Performance
![Product Analysis](screenshots/product_performance.png)
- Dual-axis chart showing quantity sold vs unit price
- Category breakdown (Fruits: 58%, Vegetables: 42%)
- Discount impact analysis

### 3. Top Product Rankings
![Top Products](screenshots/top_products.png)
| Category              | Products                          |
|-----------------------|-----------------------------------|
| 🏆 Top 3 Most Sold    | Carrot, Tomato, Orange           |
| 📉 Top 3 Least Sold   | Kale, Celery, Brussels Sprout    |
| 💎 Top 3 Most Expensive | Asparagus, Cranberry, Raspberry |

## 🛠️ Technical Implementation
- **Data Modeling**: Star schema with proper relationships
- **DAX Measures**:
  ```dax
  Total Sales = SUM(Sales[TotalAmount])
  Avg Discount = AVERAGE(Sales[Discount]) 
# data-analysis-project-
Created an interactive dashboard using Power BI to analyze and visualize key insights from the dataset. Included data cleaning, transformation, and visualization to support decision-making.
