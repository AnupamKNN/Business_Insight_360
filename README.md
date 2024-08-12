# Business Insight 360

[Link to Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNTlkZjBhZDgtMmU4NC00Y2IyLTk2YTMtZjRhNGRiYmY5MGQ4IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Project Overview

AtliQ Hardware has experienced rapid growth over the past few years and has now decided to utilize PowerBI for data analytics within the company for the first time. This strategic move aims to outpace their market competitors and enable data-driven decision-making. The project is expected to address stakeholder inquiries across various aspects, including finance, sales, marketing, and supply chain.


I completed this project by following the Codebasics Data Analyst Bootcamp 2.0. The course link is [Link](https://codebasics.io/bootcamps/data-analytics-bootcamp-with-practical-job-assistance)

[Live Report Link]

## Technology framework
- SQL
- Microsoft Power BI
- Microsoft Excel
- DAX Language
- DAX Studio (for report optimization)
- Project Charter File

## PowerBI approaches understood
- What are all the inquiries that should be addressed before initiating the project?
- Creating Calculated Columns
- Creating Measures using Dax Language
- Data Modeling (Star Schema, Snowflake Schema)
- Employing Bookmarks for toggling between two visuals
- Navigating between pages using buttons
- Utilizing the divide function to mitigate zero division errors
- Generating a date table using M language
- Dynamic titles determined by the applied filters
- Using KPI indicators
- Applying conditional formatting to visuals by utilizing icons or background color
- Data validation techniques
- Power Bi Service
- Publishing reports to PowerBi services
- Establishing a personal gateway to automate the data refresh process
- Power BI app creation
- Collaboration, workspace management, and access permissions in Power BI Service
- Etc. 😊

## GitHub
- Uploading large files using GitHub LFS

- Tracking specific file extensions for LFS

## Business terminologies and lexicon
- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - Cost of Goods Sold
- YTD - Year-to-Date
- YTG - Year-to-Go
- Direct
- Retailer
- Distributors
- Consumer

## Company profile

AltiQ Hardware has experienced significant growth in recent years, expanding its business operations globally. Specializing in the sale of computers and computer accessories, the company operates through three primary channels:
- Retail
- Direct
- Distributorship

Lately, the company incurred an unexpected loss due to the opening of a store in America. This decision was based on surveys, intuition, and some Excel analysis. Meanwhile, competitors have well-equipped analytics teams to drive their decision-making processes. Consequently, AltiQ Hardware finds it imperative to establish its own analytics team to leverage data-driven insights and make informed decisions to thrive in the industry.

The project initiation meeting aimed at clarifying the project objectives and rationale, and addressing any inquiries pertaining to the project.

### Questions to consider prior to dashboard development:
- What is the primary goal behind constructing this PowerBi dashboard?
- How will we measure the success of this initiative?
- What is the projected timeline for completion?
- Are stakeholders anticipating a preview before the official release?
- What are the stakeholders' aspirations for this project?
- What concerns do stakeholders harbor regarding dashboard development?
- Who will utilize this dashboard and for what purposes?
- What specific outcomes are stakeholders anticipating upon project completion?
- What potential hurdles might we encounter during development?
- What resources/data are necessary for dashboard creation?
- Have stakeholders provided input on dashboard design and visualization preferences?

Following the project initiation meetings, the data engineering team has provided the requested data to the data analytics team. Now, let's delve into them.

### Data Set Familiarization
Having a thorough understanding of the available data is crucial for effective analysis. Prior to diving into the analysis, it's essential to gain a comprehensive understanding of the dataset.

Fact Table: This table contains transactional data, providing detailed information about each transaction.

  - gdb041:
    - dim_customer
      - 27 distinct markets (ex India, USA, spain)
      - 75 distinct customers thorough out the market
      - 2 types of platforms
        - Brick & Motors - Physical/offline store
        - E-commerce - Online Store (Amazon, flipkart)
      - Three channels
        - Retailer
        - Direct
        - Distributors
    - dim_market
      - 27 distinct markets (ex India, USA, spain)
      - 7 sub-zones
      - 4 regions
        - APAC (Asia-Pacific)
        - EU (European Union)
        - nan (North American)
        - LATAM (Latin America)
       
    - dim_product
      - Divisions
        - P & A
          - Peripherals
          - Accessories
        - PC
          - Notebook
          - Desktop
        - N & S
          - Networking
          - Storage
      - There are 14 distinct categories, such as Internal HDD and keyboards.
      - Multiple variations of the same product are available.
     
    - fact_forecast_monthly
      - This table is utilized for predicting customer needs in advance, aiding in:
        - Enhanced customer satisfaction
        - Reducing warehousing costs for storage purposes.
      - The data engineering team denormalized the table to facilitate its use as a data warehouse for analytical purposes.
      - All dates within the month will be substituted with the month's start date.
      - It will encompass all column names, with the forecasted quantity needed by the customer at the end.
    - fact_sales_monthly
      - This table is largely similar to the fact_forecast_monthly table, except that the last column contains the sold quantity instead of the forecasted value.
  - gdb056
    - freight_cost
      - This table contains information about travel costs and other expenses for each market, categorized by fiscal year.
    - gross_price
      - Contains details of gross prices associated with product codes
    - manufacturing_cost:
      - Contains details of manufacturing costs associated with product codes categorized by year.
    - Pre_invoice_dedutions
      - Contains details of pre-invoice deductions percentages for each customer, categorized by year.
    - Post_invoice_deductions
      - Details of post-invoice deductions and other deductions.

## Importing data into Power Bi
Since the database for this project is MySQL, we'll need to import the datasets into Power BI by providing the database access credentials.

## Data Model
- Data modeling is essential, serving as the foundation for reports. All visualizations will be constructed based on the data model.
- Inadequate data modeling adversely impacts the overall performance of the report.
- Ensuring adherence to best practices in data modeling is essential. You can explore this blog post to familiarize yourself with these practices: [Link to Blog Post](https://addendanalytics.com/blog/data-modelling-best-practices).
- In this project, we've implemented the Snowflake data modeling method.
  
![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/01.%20Datamodel.png)

## Dashboard designing
The team will commence visual design based on the mockups received as requirements, creating measures as needed along the way.

## Home view
In the Home view, all the view buttons will be accessible. Users can navigate to specific view pages by clicking on the corresponding buttons.
  - Finance View
  - Sales View
  - Marketing View
  - Supply Chain View
  - Executive View
  - Customer and Product Performance
  - Information Pop-up
  - Support Pop-up
  
## Summative Report

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/02.%20Overview.gif)


## Finance View

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/03.%20Finance%20View.gif)


## Sales View

[](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/04.%20Sales%20View.gif)


## Marketing View

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/05.%20Marketing%20View.gif)


## Supply Chain view

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/06.%20Supply%20Chain%20View.gif)


## Executive View

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/07.%20Executive%20View.gif)


## Customer and Product Performance

![](https://github.com/AnupamKNN/Business_Insight_360/blob/main/Resources/08.%20Customer%20and%20Product%20Performance.gif)


## Project Outcome
This report serves as a valuable tool for data-driven decision-making. It enables the exploration and resolution of numerous "why" questions based on various situations and scenarios.
