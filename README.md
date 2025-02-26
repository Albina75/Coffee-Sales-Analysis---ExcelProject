# Coffee Sales Analysis using Excel
## Skills & Tools
+ Excel Formula: VLOOKUP, INDEX-MATCH, and IFS to integrate datasets.
+ Data Formatting & Structuring
+ Pivot Tables & Charts
+ Interactive Dashboard Creation

## Dashboard

![CoffeeSalesDashboard](https://github.com/user-attachments/assets/af4d7776-1221-4fbf-84e8-b257bb917c5d)

## Introduction:

In this project, I worked on analyzing coffee sales data using Excel. This involved working with three datasets—Orders, Customers, and Products—to generate insights and create a dynamic sales dashboard. This project demonstrates my proficiency in Excel formulas, data cleaning, pivot tables, and dashboard creation.





## Data Preparation and Integration

The dataset consisted of three sheets:

+ Orders: Contains order details (Order ID, Date, Customer ID, Product ID, Quantity).

+ Customers: Holds customer details (Name, Email, Country, etc.).

+ Products: Lists coffee details (Coffee Type, Roast Type, Size, Price, etc.).

To enrich the Orders table, I integrated additional customer and product information using the following formulas:

+ Customer Name: =VLOOKUP(C2,customers!$A$1:$I$1001,2,FALSE)

+ Email: =IF(VLOOKUP(C2,customers!$A$1:$I$1001,3,FALSE)=0,"",VLOOKUP(C2,customers!$A$1:$I$1001,3,FALSE))

+ Country: =VLOOKUP(orders!C2,customers!$A$1:$I$1001,7,FALSE)

+ Product Details: =@INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

+ Sales Calculation: =L2*E2

## Data Cleaning and Formatting

+ Converted date format to 05-Sep-2019 to avoid confusion.

+ Formatted sizes (e.g., 1 kg, 0.5 kg) for clarity.

+ Handled duplicates and ensured data integrity.

+ Converted range into a Table for dynamic updates.

## Dashboard Creation

Using pivot tables, I analyzed sales trends and created a dashboard:

+ Total Sales Over Time: Pivot table with Year & Month as rows, Sales as values, and Coffee Type as columns.

+ Filters & Interactivity: Added Timeline for date selection and slicers for Coffee Type, Roast Type, and Size.

+ Sales by Country: Pivot table & bar chart visualizing regional performance.

+ Top Customers: Identified top 10 customers by sales volume.

## Business Impact

This analysis provides businesses with:

+ Sales trends insights to forecast demand.

+ Customer segmentation to tailor marketing efforts.

+ Regional sales performance for strategic expansion.
