# Superstore-Sales-Analysis-

## Table of content

- [Project Overview](#project-overview)
- [Key Objectives](#key-objectives)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [EDA](#eda)
- [Data Analysis](#data-analysis)
- [Key Findings/Results](#key-findings-results)
- [Recomendations](#recomendations)
  

### Project Overview
This project analyzes Superstore customer sales data to identify trends, customer behavior, and product performance for business improvement.

### Key Objectives
1. Analyze sales performance over time
2. Understand customer behavior and purchasing patterns

### Data Sources
- Data Source: Sample Superstore.csv dataset containing sales data from 2014 to 2017 {https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data}


  ### Tools:
   Excel (data cleaning), SQL Server (data analysis), Power BI (data visualization & dashboard)

  ### Data Cleaning

Objective
To ensure data quality and prepare the Superstore sales dataset for analysis.

Tasks Performed
1. Data Loading and Inspection: Loaded the dataset and inspected for inconsistencies and errors.
2. Fixing Un-standardized Date Format: Standardized the date format to ensure consistency.
3. Handling Duplicates: Identified and handled duplicate records to prevent data redundancy.
4. Data Cleaning and Formatting: Cleaned and formatted the data to ensure accuracy and consistency.

Next Steps
The cleaned dataset is now ready for Exploratory Data Analysis (EDA) to identify trends, patterns, and insights. Some potential areas of exploration include:

- Sales trends
- Customer behavior
- Product performance
- Regional sales patterns

### Exploratory Data Analysis (EDA): 
1. What are our sales by state and city?
2. List our top 10 performing sub-category based on profit.
3. Average sales by category
4. Who are our top 10 customers?
5. What are our sales by segments?

  ###  Data Analysis
  ```sql
  SELECT State, City, SUM(Sales) AS Sales_by_location
FROM Supperstore_Customer
GROUP BY State, City
ORDER BY Sales_by_location DESC;

SELECT top 10 Sub_Category, SUM(Profit) AS TotalProfit
FROM Supperstore_Customer
GROUP BY Sub_Category
ORDER BY TotalProfit DESC;

SELECT Category, AVG(Sales) AS Sales_by_category
FROM Supperstore_Customer
GROUP BY Category
ORDER BY Sales_by_category DESC;

SELECT top 10 Customer_Name, SUM(Sales) AS TotalPurchase
FROM Supperstore_Customer
GROUP BY Customer_Name
ORDER BY TotalPurchase DESC;

SELECT Segment, SUM(Sales) AS Sales_by_segment
FROM Supperstore_Customer
GROUP BY Segment
ORDER BY Sales_by_segment DESC;
```

### Key Findings/Results
1. Steady Sales Growth: Overall sales trend shows steady growth with seasonal fluctuations.
2. Key Customers: Top 10 customers contribute significantly to sales.
3. High-Performing Sub-Categories: Copiers and Phones sub-categories drive sales and profitability.
4. Regional Variations: Sales vary by region, with the South Region leading the pack.
5. Segment-Specific Sales: Consumer, Corporate, and Home Office segments have distinct sales patterns.

### Recomendations
Base on the analysis i recomend the folllowing actions
1. Invest in marketing and promotion in categories that are not striving in sales
2. Enhance Customer Relationships
3. Loyalty Programs: Implement loyalty programs to retain high-value customers.
4. Personalized Service: Offer personalized service to key accounts to build strong relationships and increase customer satisfaction.
This will help retain valuable customers and improve overall customer satisfaction in all region.




