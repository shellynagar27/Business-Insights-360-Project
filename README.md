# Business-Insights-360-Project
I built this project by following the [Codebasics PowerBi Course](https://codebasics.io/courses/power-bi-data-analysis-with-end-to-end-project)
## Live Dashboard Link:
   - [Business Insights 360 (older Version)](https://app.powerbi.com/view?r=eyJrIjoiYjg5MzAwZDAtN2VjZi00ZTRlLWExOTItOTFlNjFkODE0NjRlIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&embedImagePlaceholder=true&pageName=a6526f176bdc85783e3a)
   - [Business Insights 360 2.0 (new Version)](https://app.powerbi.com/view?r=eyJrIjoiOWYzZGNjNmUtZmEyMS00ZmU1LThlNDUtNjhhOWJmMjMyM2ZiIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&embedImagePlaceholder=true&pageName=c5dd4a35405ee38145b0)
   - [Linkedin Post](https://www.linkedin.com/feed/update/urn:li:activity:7240827643636391936/)
## Problem Statement
   AtliQ Hardware (Imaginary Company) has experienced rapid growth in recent years and decided to implement data analytics using Power BI for the first time to outpace competitors and make data-driven decisions. This project aims to address stakeholders' questions across finance, sales, marketing, and supply chain aspects.
## Dataset Understanding
Dataset has two type of tables:
   * Dimension Tables: Data is mostly statics and consist unique values
   * Fact Table: Store transactions
### MySQL Data Source
#### gdb041

###### dim_customer
- **Distinct Markets**: 27 (e.g., India, USA, Spain)
- **Distinct Customers**: 75 across the markets
- **Types of Platforms**:
  - Brick & Mortar: Physical/offline stores
  - E-commerce: Online stores (e.g., Amazon, Flipkart)
- **Channels**:
  - Retailer
  - Direct
  - Distributors

###### dim_market
- **Distinct Markets**: 27 (e.g., India, USA, Spain)
- **Sub-zones**: 7
- **Regions**:
  - APAC
  - EU
  - NAN
  - LATAM

##### dim_product
- **Divisions**:
  - P & A
    - Peripherals
    - Accessories
    - PC
      - Notebook
      - Desktop
  - N & S
    - Networking
    - Storage
- **Categories**: 14 (e.g., Internal HDD, Keyboard)
- **Variants**: Different variants available for the same product

##### fact_forecast_monthly
- **Purpose**: Forecasts customer needs in advance
  - **Benefits**:
    - Higher customer satisfaction
    - Reduced warehouse storage costs
- **Data**:
  - Denormalized for analytical use
  - Dates replaced by the start date of the month
  - Includes forecast quantity needed by the customer

##### fact_sales_monthly
- **Purpose**: Similar to `fact_forecast_monthly`
  - **Difference**: Last column contains sold quantity instead of forecast quantity

#### gdb056

##### freight_cost
- **Details**: Travel and other costs for each market, including fiscal year

##### gross_price
- **Details**: Gross prices with product codes

##### manufacturing_cost
- **Details**: Manufacturing costs with product codes and year

##### pre_invoice_deductions
- **Details**: Pre-invoice deductions percentage for each customer, with year

##### post_invoice_deductions
- **Details**: Post-invoice and other deduction details
### Excel files:
   ##### **marketshare-v2022**: contains market share info as per sub_zone and product cateogory for various companies
   ##### **targets**: net sales, net profit and gross margin target on momth-year basis for different countries
   ##### **operating-expenses-table**: Operatinf expenses as per fiscal year for various countries
## Data Model
![Screenshot 2024-09-20 235340](https://github.com/user-attachments/assets/a8fbccf4-0420-4f7a-b036-aa3d63fad849)

## Steps Taken
   * Imported data using MySQL, Excel, and text files, and set up automated data refreshing via Power BI Services, Microsoft Teams, Gateways, and SharePoint.
   * Validated data with MySQL, optimized queries to reduce file size and loading time, and used tools like Performance Analyzer and DAX Studio.
   * Created Measures as per need for creating visuals and KPI cards.
   * Created a comprehensive dashboards for various teams like finance, sale, marketing and supply chain, and for that created needed measures and tables
   * Designed an executive dashboard showcasing top customers/products, financial trends, market positioning, and competitor analysis.
   * Utilized field parametes for dynamic target setting and learned the significance of UAT and stakeholder mapping
## Key learnings
   * Learned OLTP & OLAP concepts, data warehousing, star and snowflake schemas, and query folding.
   * Mastered new DAX functions (e.g., ALLNOBLANKROWS, ABS, SWITCH, FILTER, HASONEVALUE) and applied them in Power BI.
   * Learned concepts of Project charter, User Acceptance Testing, and Stakeholdr Mapping and their importance
   * Understand the concept of star and snowflakes schema and need of dimension table
   * Learned new features of Power BI like new card visual, conditional formatting, Ribbon chart, water fall chart etc.
   * Learned new terms and their use case like forecast accuracy, net error, absolute error, ytd, ytg and landing estimate
   * Built an understanding of important factors and KPIs for different teams like finance, sales, marketing, supply chain and executive view.
   * Learned meaning of query folding with practical example.
   * Publishing of Report on Power BI Services, setting up of personal gateway for automatic data refresh from MySQL and usage of Microsoft Share Point for automatice refresh of other types of files like-Excel & CSV
## Features
   * Info and Support Page
   * Use of Bookmark Buttons to toggle between visuals
   * Usage of Tooltips for more better understanding
   * Slicer to compare various parameters based on Last year and Targeted Value
   * Usage of various symbols and conditioanl formatting for better data understanding
## Dashboard Contain Following Pages:
   * Home
   * Info
   * Support
   * Finance View
   * Sales View
   * Marketing View
   * Executive View
## Designing of Dashboards:
   Dashboards are designed as per the mocks and with suitable adjustments to catter various visualization needs.
## Outcome
Delivered a comprehensive understanding of the business's market standing, identified focus areas for optimization, highlighted underperforming customers, and provided year-wise financial insights, aiding in better inventory planning and performance tracking. Further it can be used in answering n number of why questions based on the situations.
## Tools Used:
   * Power BI
   * MySQL
   * DAX Studio
   * [Freepik](https://www.freepik.com/)
   * [flaticon](https://www.flaticon.com/)
   * [Figma](https://www.figma.com/)
   * [Coolors](https://coolors.co/palettes/trending)
