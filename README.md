# Adventure Works - Sales KPI

### Dashboard Link : https://docs.google.com/spreadsheets/d/13hSVy2znulV3emNhgHvvnjhGjZfgYUFU/edit?usp=drive_link&ouid=115038762084746239933&rtpof=true&sd=true

## Problem Statement

The stakeholders need your report to answer a 
variety of KPI-related questions, including:
- What are the total sales and average sales?
- What are the monthly total sales?
- What is the total number of orders placed during this time period?
- What is the total marketing expenditure, and what is the monthly marketing expenditure?
- What is the change in sales over time for the sales teams, and how does this correlate with marketing spending?
- What sales region had the highest sales during this time period, and how did their ranking change over time?
- What is the performance of different sales regions with their advertising campaigns?
To complete this task, your manager provides you with a sales dataset for the last three 
months containing total sales volume and advertising spending for various sales regions. Each of these regions runs different advertising campaigns (Indicating business performance)


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.
- Step 2 : Open the Model View and create new table by using the following DAX code:

        Date = 
            ADDCOLUMNS (
                    CALENDAR (MIN ('Exercise 5 1 4 6-Update'[OrderDate]), 
                    MAX ('Exercise 5 1 4 6-Update'[OrderDate])),
                    "Year", YEAR ([Date]),
                    "MonthNumber", MONTH ([Date]),
                    "MonthName", FORMAT ([Date], "MMMM")
            )
- Step 3 : Then right click on the Data table and select "Mark as Date table".
- Step 4 : Create a relationship between the Date field on Date table and the OrderDate on the main table.
- Step 5 : Now return to Report View to start building you report with the following Steps:

   (a) Add a Multi-row card to the convas and on the field select MonthName and SalesAmount.

   (b) Add other Multi-row card to the canvas and on the field select MonthName and MarketingSpend.

   (c) Add 4 cards in the first one select SalesAmount, and in the second one select salesAmount and change from SUM to Average, and for the third select SalesID and change from SUM to Count, and finaly the last on select MarketingSpend.

   (d) Add Waterfall chart and on category field select MonthName, on Breakdown field select SalesTeam, on Y-axis select SalesAmount.

   (e) Add Ribbon chart and on X-axis select MonthName, on Y-axis select SalesAmount, on Legend select Region.

   (f) Add Slicer and select SalesTeam.
- Step 6 : Now arrange the visuals to start the design part.
- Step 7 : For design I used MS Power Point you can use whatever you want.

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Total Sales = 1.04 M
### [2] Average Sales = 64.75 K
### [3] Total Order = 16
### [4] Total Marketing Spend = 126 K
#### a) On July   = 68200
#### b) On June   = 30500
#### c) On May    = 27000
### [5] The report shown that the Team B get big number of Sales Amount than Team A.
### [6] The East region had the highest sales.
