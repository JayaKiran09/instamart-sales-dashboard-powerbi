# Instamart Sales Performance Dashboard — Power BI:
An end-to-end Business Intelligence project: cleaning messy retail data, modeling it into a star schema, and building an interactive 3-page dashboard for a fictional online grocery chain (Instamart) operating across Tier 1–3 cities in India.

🎯 Project Goal:
Instamart's leadership needed a single source of truth to track sales performance across outlets, product categories, and cities — built from four raw, uncleaned CSV extracts.

🧹 Data Cleaning (Power Query):
The source data (~10,700 sales transactions, 500 products, 50 outlets, 2,000 customers) had realistic real-world issues, all resolved inside Power Query — no Excel pre-cleaning:
Removed ~250 duplicate transaction rows and blank rows.
Standardized inconsistent text (Low Fat / LOW FAT / low fat → Low Fat; tier 1 / TIER 1 → Tier 1; M/male/MALE → Male).
Fixed misspelled outlet types (Supermarkt, Super Market → Supermarket).
Converted text-typed numeric/date fields to proper types (DD-MM-YYYY parsing, Sales/Quantity/Rating to numeric).
Identified and handled outliers (negative sales, 9,999,999 sales values, ratings outside 1–5).
Trimmed whitespace across all text columns.

⭐ Data Model:
Built a star schema with Fact_Sales as the central fact table, connected via single-direction Many-to-One relationships to three dimension tables: Dim_Product, Dim_Outlet, and Dim_Customer.

📐 DAX Measures & Calculated Columns:
Core measures: Total Sales, Total Transactions, Total Quantity, Average Sales, Average Rating, Avg Sales per Outlet.
Time intelligence: Sales YoY Growth % using CALCULATE + SAMEPERIODLASTYEAR.
Calculated columns: Sales Band (Low/Medium/High), Outlet Age, Rating Category (Poor/Average/Good).

📊 Dashboard Pages:
Executive Summary — KPI cards, sales trend over time, sales by outlet type, sales by fat content, sales by city (map), year/tier/outlet-type slicers.
Product & Category Analysis — Top 10 items by sales, sales by category & fat content, category performance matrix with conditional formatting.
Outlet Performance — Sales by outlet size, outlet-level performance breakdown.

🛠️ Tools:
Power BI Desktop · Power Query (M) · DAX

📁 Files:
InstamartDashboard.pbix — the full Power BI report
Fact_Sales.csv, Dim_Product.csv, Dim_Outlet.csv, Dim_Customer.csv — source data
/screenshots — dashboard page exports

🔑 Key Takeaways:
Tier 1 outlets drive 60% of revenue but Tier 3 outlets show the highest YoY growth.
