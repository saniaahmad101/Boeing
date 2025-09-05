🛫 Boeing Analytics — SQL to Visual Insights
This project provides an end-to-end pipeline for analyzing Boeing aircraft, customer, and financial datasets. It uses SQL for data extraction and transformation and Power BI for semantic modeling and visualization, enabling reproducible, business-ready insights.

🗄️ Data Architecture
Source Datasets
Structured SQL tables representing:
aircraft — model, entry into service, performance metrics
orders — airline customer, region, order year, order quantity
maintenance — reliability events, malfunction types, cost categories
fuel_ops — flight hours, fuel burn, efficiency ratios
financials — R&D spend, operating margins, ROI, revenue by segment
SQL Layer
ETL scripts standardize field naming and enforce referential integrity (e.g., aircraft_id, customer_id).
Window functions applied for trend analysis (e.g., rolling averages of order growth).
Aggregation queries generate KPI tables for visualization (orders_by_region, fuel_efficiency_summary, etc.).
Data Modeling (Power BI)
Star schema: fact tables (orders, maintenance, fuel_ops, financials) join with dimension tables (aircraft, customers, regions).
Relationships defined on surrogate keys (aircraft_id, customer_id, region_id).
DAX measures created for calculated KPIs (e.g., AvgFuelBurnPerHour, OrderGrowthYoY, ROICalc).

📊 Dashboards
Aircraft Reliability — Failure rates, MTBF, maintenance cost per model.
Global Orders Heatmap — Geographic distribution of Boeing orders.
Fuel Efficiency — Fuel burn trends by aircraft family and customer.
Financial KPIs — ROI, margin trends, and R&D intensity benchmarks.
Customer Value — Profitability ranking and order activity by airline.
Trend Analysis — Long-term demand cycles and delivery growth.

⚙️ Tech Stack
Database: SQL (ANSI-compliant queries, tested on PostgreSQL & SQL Server).
Visualization: Power BI (Data Model, DAX, custom visuals).
Version Control: GitHub for SQL scripts, .pbix files, and documentation.
Optional: Python (Pandas/NumPy) for preprocessing and validation.

🚀 Getting Started
Clone repository and set up SQL database.
Run ETL scripts in /sql to create base and summary tables.
Open the .pbix file in Power BI and refresh connections.
Explore dashboards and customize DAX measures as needed.
