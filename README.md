# Supply-Chain-Data-Engineering
This project focuses on optimizing supply chain operations through data engineering and analytics. It involves building an ETL pipeline, applying data cleaning and transformation, and creating a data warehouse using the Star Schema model.

Project Structure

The project is divided into four main parts:

ETL Pipeline:
Extracted raw supply chain data, cleaned inconsistencies (dirty & messy data), transformed it into a structured schema, and loaded it into a database.

Data Modeling:
Designed a Star Schema including:

Fact Table: fact_orders_and_shipments

Dimension Tables: DimProduct, DimCustomer, DimDate, DimWarehouse, DimShipment

Data Analysis and Visualization:
Created dashboards in Power BI to analyze shipment performance, delay rates, customer regions, and delivery timelines.

Future Extension (Optional):
The cleaned and structured data can be extended for predictive modeling — e.g., shipment delay forecasting or warehouse efficiency optimization.

⚙️ ETL Pipeline Steps

Extract:
Loaded the dataset orders_and_shipments.csv using pandas.

Transform:

Cleaned data issues such as inconsistent country names and incorrect data types.

Created new columns (Shipping Time, Shipment Status) to track delays.

Developed dimension tables with surrogate keys and removed duplicates.

Merged data into a fact table referencing all dimension tables through foreign keys.

Load:

Exported dimension and fact tables as .csv files.

Loaded all tables into an SQLite database for query analysis.

🗃️ Data Model (Star Schema)

Fact Table:
fact_orders_and_shipments — contains measures like Profit, Gross Sales, Discount %, Shipping Time, and foreign keys referencing dimensions.

Dimension Tables:

DimProduct: Product details (department, category, name)

DimCustomer: Customer attributes (market, region, country)

DimDate: Order date details

DimWarehouse: Warehouse locations

DimShipment: Shipment details (mode, delay status, days scheduled)

📊 Power BI Insights

The analytical dashboard provides:

Delay Rate by Region: Identify regions with the highest shipment delays.

Monthly Shipment Count & Delay %: Track performance trends over time.

Average Scheduled vs Actual Days: Evaluate delivery performance by shipment status.

Late vs On-time % by Shipment Mode: Assess the reliability of each shipment method.

(Refer to the dashboard image below)


🧠 Key Learnings

Built an end-to-end data engineering pipeline using Python & SQLite.

Applied data cleaning, feature engineering, and data modeling principles.

Designed a data warehouse optimized for analytical queries and BI tools.

Generated actionable insights on shipment delays and regional performance.

🛠️ Technologies Used

Python (Pandas, SQLite3)

Power BI

SQL

Data Modeling (Star Schema)

Data Cleaning and Transformation
