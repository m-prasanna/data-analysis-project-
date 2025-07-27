# Power BI Sales & Inventory Dashboard

## 📌 Project Aim
To analyze fruit/vegetable sales data and provide actionable insights for:
- Inventory optimization
- Customer segmentation
- Pricing strategy improvement

## 📂 Dataset Overview
**Source:** Excel workbook with 3 tables

### 1. Sales (357 records)
Columns: 
- CustomerID, ProductID, Quantity, UnitPrice, Discount, TotalAmount

### 2. Products (25 items)
Columns:
- ProductID, Name, Category (Fruit/Vegetable), UnitPrice

### 3. Customers (12 records)
Columns:
- CustomerID, Name, Country, Gender, BirthYear

## 📋 Requirements Implemented
1. **Customer Analysis**
   - Most quantity purchased by customer
   - Amount by gender and birth year

2. **Product Analysis**  
   - Quantity, total amount and unit price by product
   - Category comparison (Fruit vs Vegetable)

3. **Top Product Rankings**
   - Top 3 most/least sold products
   - Top 3 most expensive products

4. **Key Metrics Cards**
   - Total sales
   - Total discount given
   - Total quantity sold

## 🖥️ Dashboard Components

### Main Page
- **Customer Insights Section**
  - Bar chart: Top customers by quantity purchased
  - Donut chart: Gender distribution
  - Line chart: Purchases by birth year

- **Product Performance Section**
  - Scatter plot: Quantity vs Unit Price
  - Stacked column: Sales by category
  - Table: Complete product list with metrics

- **Executive Summary Cards**
  - Total sales: $1,247.82
  - Total discount: $103.45
  - Total quantity: 642 units

### Filters Panel
- Product category toggle
- Country selector
- Date range (if applicable)

## 🔍 Key Findings
1. **Customer Trends**
   - Female customers purchase 23% more than males
   - Bulk buyers concentrated in Netherlands

2. **Product Insights**
   - Carrot is best-selling (87 units)
   - Asparagus has highest margin (38%)
   - Kale has lowest turnover (12 units)

## 🛠️ Technical Details
**Data Model:**
- Star schema with relationships
- 3 fact tables, 2 dimension tables

**DAX Measures:**
```dax
Total Sales = SUM(Sales[TotalAmount])
Profit Margin = DIVIDE([Total Sales]-[Total Cost],[Total Sales])
