# Transforming-Business-Operations-with-Power-BI-Analytics

## Project Overview

AtliQ Hardware has been experiencing significant growth in recent years and has decided to implement data analytics through Power BI for the first time. The goal is to outperform competitors in the market and make data-driven decisions. This project aims to provide insights across various business areas, including finance, sales, marketing, and supply chain, in order to address stakeholder queries.


## Tech Stack

- SQL
- Power BI Desktop
- Excel
- DAX Language
- DAX Studio (for report optimization)
- Project Charter File

## Power BI Techniques Learned

- Key questions to ask before starting a project
- Creating calculated columns
- Creating measures using DAX
- Data modeling
- Using bookmarks to toggle between visuals
- Page navigation with buttons
- Preventing zero division errors with the DIVIDE function
- Creating date tables using M language
- Creating dynamic titles based on applied filters
- Using KPI indicators
- Applying conditional formatting with icons or background color
- Data validation techniques
- Power BI Services
- Publishing reports to Power BI Services
- Setting up personal gateway for data auto-refresh
- Creating Power BI apps
- Managing collaboration, workspace, and access permissions in Power BI Services

## Business Terminology

- Gross Price
- Pre-Invoice Deductions
- Post-Invoice Deductions
- Net Invoice Sales
- Gross Margin
- Net Sales
- Net Profit
- COGS (Cost of Goods Sold)
- YTD (Year to Date)
- YTG (Year to Go)
- Direct
- Retailer
- Distributors
- Consumer

### Dataset Understanding

A clear understanding of available data is crucial before diving into analysis. It’s important to familiarize yourself with the data you will be working with.

**Dimension Tables**: Contain static data, such as customer and product details.

**Fact Tables**: Contain transactional data.

- **gdb041**:
    - **dim_customer**:
        - **27** distinct markets (e.g., India, USA, Spain)
        - **75** distinct customers across all markets
        - **2** platform types: 
            - Brick & Mortar (Physical store)
            - E-commerce (Online stores like Amazon, Flipkart)
        - Three distribution channels: 
            - Retailer 
            - Direct 
            - Distributors
    - **dim_market**:
        - **27** distinct markets (e.g., India, USA, Spain)
        - 7 sub-zones
        - 4 regions: APAC, EU, LATAM, and NAN
    - **dim_product**:
        - Divisions: 
            - P & A (Peripherals, Accessories)
            - PC (Notebook, Desktop)
            - N & S (Networking, Storage)
        - 14 categories (e.g., Internal HDD, keyboard)
        - Multiple variants for each product
    - **fact_forecast_monthly**:
        - Used for forecasting customer demand to improve satisfaction and reduce storage costs.
        - Denormalized for analytical use by the data engineering team.
        - Replaces all dates with the start date of the month and includes forecasted quantity.
    - **fact_sales_monthly**:
        - Similar to the forecast table but contains actual sales data instead of forecasts.
- **gdb056**:
    - **freight_cost**: Details of travel and other costs by market and fiscal year.
    - **gross_price**: Details of gross prices by product code.
    - **manufacturing_cost**: Details of manufacturing costs by product code and year.
    - **pre_invoice_deductions**: Pre-invoice deduction percentages for each customer.
    - **post_invoice_deductions**: Details of post-invoice deductions.

## Importing Data into Power BI

Since the database in this project is MySQL, the datasets are imported into Power BI by providing the necessary database access credentials.

## Data Modeling

Data modeling is the foundation of the report, and all visuals are built upon it. Poor data modeling can negatively affect report performance, so following best practices is essential. For reference, see this [Blog](https://addendanalytics.com/blog/data-modelling-best-practices/). In this project, we’ve used the Snowflake Data Modeling method.

<img src="https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/data_model.png" class="center">

### Dashboard Design

The team designs visuals based on the requirements received in the form of mockups. Measures are created as needed during this process.

## Home View

The Home view provides buttons to navigate to specific report sections:

- Info
- Finance View
- Sales View
- Marketing View
- Supply Chain View
- Executive View
- Products
- Support

## Finance View

![Finace.png](https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/Finance%20view.png)

## Sales View

![Sales.png](https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/Sales_view.png)

## Marketing View

![Marketing.png](https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/Marketing_view.png)

## Supply chain View

![Supply chain.png](https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/Supply%20chain.png)

## Executive View

![Executive.png](https://github.com/wekey1998/Transforming-Business-Operations-with-Power-BI-Analytics/blob/main/Executive%20view.png)

## Project Outcome

This report enables data-driven decision-making and provides answers to numerous "why" questions based on specific scenarios.
