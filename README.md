# Adventure Works - Dashboard

### Dashboard Link : https://drive.google.com/drive/folders/1QDLn72f8EQcCamSWXE9uTMGwxo_EZjGE

## Problem Statement
The company faces challenges in effectively monitoring and analyzing its sales performance, revenue generation, profit margins, and product returns. Additionally, there is a need to compare regional performance, identify product-level trends, and recognize high-value customers to drive strategic decision-making. The existing data is scattered across multiple sources, lacks integration, and is not readily available for comprehensive analysis.

To address these challenges, a solution is required that can:

Consolidate Data: Integrate data from various sources including sales databases, CRM systems, and spreadsheets.

Transform and Model Data: Clean, transform, and model the data to ensure consistency and accuracy for analysis.

Advanced Calculations: Utilize advanced DAX calculations to derive key metrics and insights.

Interactive Visualization: Provide an interactive, user-friendly dashboard that visualizes KPIs, regional performance, product trends, and customer insights.

Real-Time Updates: Enable real-time data updates to ensure stakeholders have access to the latest information.

Detailed Analysis: Allow detailed drill-down and drill-through capabilities for in-depth analysis.

By addressing these needs, the company aims to enhance its ability to monitor performance, make informed decisions, and ultimately drive business growth and efficiency.

### Snapshots

- 
  Calculated column was created in which, customers were parents or not,

for creating new column following DAX expression was written;
       

        Parent = IF('Customer Lookup'[TotalChildren]>0, "YES", "NO")

Snap of new calculated column ,

![calculated_col](https://github.com/Manojgowda2000/AdventureWorks/assets/107106672/5415f9c1-f2d7-4c07-bd37-a76e724f805e)

        
- New measure was created to find total count of customers who made transactions.

Following DAX expression was written for the same,
        
        Total customers = DISTINCTCOUNT('Sales Data'[CustomerKey])
 
A card visual was used to represent count of customers.

![Customers](https://github.com/Manojgowda2000/AdventureWorks/assets/107106672/3196c0e2-3316-4614-a997-abf1f0069a57)


        
 - New measure was created to find the total revenue,
 
 Following DAX expression was written to find revenue,
 
        Revenue = SUMX('Sales Data','Sales Data'[OrderQuantity]*RELATED('Product Lookup'[ProductPrice] ))
 
 A card visual was used to represent.
 
 ![Revenue](https://github.com/Manojgowda2000/AdventureWorks/assets/107106672/8b193031-63bf-4f60-b9d4-ff10e4241ae8)

 
 - The report was then published to Power BI Service.
 
 
![Publish](https://github.com/Manojgowda2000/AdventureWorks/assets/107106672/b4b7eab0-6024-4e7a-997e-22bdadd346b6)


# Snapshot of Dashboard (Power BI Service)

![Dashboard](https://github.com/Manojgowda2000/AdventureWorks/assets/107106672/7b78888c-cdc7-4463-9acf-a699334d34f0)

