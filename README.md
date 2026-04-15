# 📊 Blinkit Data Analysis Project

<div align="center">

<img width="1391" height="732" alt="Image" src="https://github.com/user-attachments/assets/76c3a828-dfe8-4fea-b126-5da9b891d4f6" />

<br/>
<br/>

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge&logo=powerbi)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Excel-Data%20Source-217346?style=for-the-badge&logo=microsoftexcel)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![Python](https://img.shields.io/badge/Python-Preprocessing-blue?style=for-the-badge&logo=python)](https://www.python.org/)

</div>

---

## 📌 Table of Contents

- [Case Study](#-case-study)
- [Dashboard Preview](#-dashboard-preview)
- [Database Description](#-database-description)
- [Data Cleaning](#-data-cleaning)
- [Data Analysis and Insights](#-data-analysis--insights)
- [Measures and DAX Formulas](#-measures--dax-formulas)
- [Tools and Technologies](#-tools--technologies)
- [How to Use](#-how-to-use)

---

## 📌 Case Study

**Blinkit** is one of India's leading quick-commerce grocery delivery companies.
This project analyzes **sales, product categories, outlet performance, and customer preferences** to generate actionable insights.

### Objective

- 🎯 Identify key factors influencing sales performance
- 📈 Provide recommendations to improve revenue and outlet efficiency
- ⭐ Enhance customer satisfaction through data-driven decisions

---

## 📊 Dashboard Preview

<img width="1412" alt="Blinkit Data Analysis Dashboard" src="https://github.com/user-attachments/assets/f5464490-1f51-4b35-993b-ea4d7f1a349e" />

---

## 🗄️ Database Description

The dataset **`BlinkIT Grocery Data.xlsx`** consists of transactional and categorical information about grocery items sold across different outlets.

### Table — Grocery Sales Data

| Column Name | Description |
|-------------|-------------|
| **Item Identifier** | Unique product code for each grocery item |
| **Item Fat Content** | Type of fat content (Low Fat, Regular, etc.) |
| **Item Type** | Category of product (Fruits, Frozen Foods, Canned, Soft Drinks, etc.) |
| **Item Weight** | Weight of the item in kilograms |
| **Item Visibility** | Proportion of display area allocated to the item in the store |
| **Outlet Identifier** | Unique ID for each store |
| **Outlet Establishment Year** | Year when the outlet was established |
| **Outlet Location Type** | Tier of the outlet location (Tier 1, Tier 2, Tier 3) |
| **Outlet Size** | Size of the outlet (Small, Medium, High) |
| **Outlet Type** | Type of supermarket (Supermarket Type1, Type2, Type3, Grocery Store) |
| **Sales** | Total sales value of the product |
| **Rating** | Customer rating for the product (scale of 1–5) |

---

## 🧹 Data Cleaning

| Step | Action |
|------|--------|
| ✅ Missing Values | Handled missing values in `Item Weight` and `Sales` columns |
| ✅ Standardization | Standardized categorical fields e.g. `LF` and `low fat` → `Low Fat` |
| ✅ Outliers | Treated outliers in `Item Visibility` and `Sales` |
| ✅ Encoding | Encoded categorical variables for analysis |

---

## 📈 Data Analysis & Insights

### Dataset Summary

| Metric | Value |
|--------|-------|
| 📌 Total Records | **8,523** |
| 📦 Unique Items | **1,559** |
| 🏬 Unique Outlets | **10** |
| 💰 Total Sales | **₹1.2M** |
| 📉 Average Sales per Item | **₹141** |

### Key Insights from Dashboard

<details>
<summary><b>💰 Sales Performance</b></summary>
<br>

- **Total Sales** reached **$444.79K** across all outlets
- **Average Sales** per item stands at **$142**
- **Supermarket Type1** dominates with **$362.60K** in total sales
- **Grocery Stores** contribute **$82.19K** with 585 items

</details>

<details>
<summary><b>🛒 Fat Content Analysis</b></summary>
<br>

- **Low Fat** products account for **$315.23K** in sales
- **Regular** fat products contribute **$129.57K**
- Tier 2 outlets lead with **$0.18M** in Low Fat sales
- Tier 1 contributes **$0.13M** in Low Fat sales

</details>

<details>
<summary><b>🏷️ Top Performing Item Types</b></summary>
<br>

| Item Type | Sales |
|-----------|-------|
| Snack Foods | $61K |
| Fruits and Vegetables | $60K |
| Household | $59K |
| Frozen Foods | $44K |
| Dairy | $36K |
| Canned | $33K |
| Health and Hygiene | $32K |
| Baking Goods | $29K |

</details>

<details>
<summary><b>🏬 Outlet Performance</b></summary>
<br>

- **Outlet Establishment** peaked around **2016–2017** with sales of **$132K–$133K**
- Sales declined post-2017 settling at **$50K** by 2020
- **Tier 2** outlets lead outlet location sales at **230.49K**
- **Tier 1** follows at **205.92K**
- **Tier 3** contributes **8.38K**

</details>

<details>
<summary><b>⭐ Customer Ratings</b></summary>
<br>

- **Average Rating** across all products is **3.9 out of 5**
- Both Supermarket Type1 and Grocery Stores maintain an average rating of **4**
- Item visibility for Grocery Stores is **0.11** vs **0.06** for Supermarket Type1

</details>

---

## 🧮 Measures & DAX Formulas

The following **DAX measures** were created in Power BI for analysis:

-- Total Sales
Total Sales = SUM('BlinkIT Grocery Data'[Sales])

-- Average Sales
Average Sales = AVERAGE('BlinkIT Grocery Data'[Sales])

-- Average Rating
Average Rating = AVERAGE('BlinkIT Grocery Data'[Rating])

-- No. of Items
No. of Items = COUNTROWS('BlinkIT Grocery Data')

-- Metrics Field Parameter
Metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Avg Sales", NAMEOF('BlinkIT Grocery Data'[Avg Sales]), 1),
    ("No. of Items", NAMEOF('BlinkIT Grocery Data'[No. of Items]), 2),
    ("Avg Rating", NAMEOF('BlinkIT Grocery Data'[Avg Rating]), 3)
}

🚀 Tools & Technologies
Category	Tool
Dashboard and Visualization	Microsoft Power BI
Data Source	Microsoft Excel
Data Preprocessing	Python and Pandas
Version Control	Git and GitHub
📂 How to Use
Bash

# Step 1: Clone the repository
git clone https://github.com/SumedhKolte/Blinkit_data_analytic_dashboard.git

# Step 2: Navigate into the project folder
cd Blinkit-Data-Analysis
Open the dataset BlinkIT Grocery Data.xlsx for reference
Load the Blinkit data analysis.pbix file in Power BI Desktop
Refresh data if needed and explore the interactive dashboards
Use the Filter Panel to slice data by Outlet Location Type, Outlet Size, and Item Type
<div align="center">
✨ This project provides data-driven insights into Blinkit's grocery sales and helps in strategic decision-making for product placement, store optimization, and customer satisfaction

<br/> <br/>
⭐ If you found this project helpful please consider giving it a star
Built with ❤️ by SumedhKolte
