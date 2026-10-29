# Sales-Performance-Target-Achievement-Analysis-Power-BI-Project
Power BI dashboard to monitor sales, profit, order volume, product and customer performance and monthly regional target achievement. 

SALES PERFORMANCE & TARGET ACHIEVEMENT REPORT

INTRODUCTION
The Sales Performance & Target Achievement Dashboard is developed using Microsoft Power BI to analyze sales data and monitor business performance. The dashboard provides insights into total sales, total orders, quantity sold, profit, regional sales performance, product-wise sales, and salesperson target achievement.

OBJECTIVES
• To analyze overall sales performance. • To monitor total orders and quantity sold. • To evaluate total profit generated. • To compare sales performance across different regions. • To identify the best-performing products. • To compare actual sales with sales targets. • To support better business decision-making using data visualization.

DATASETS USED
The project uses the following datasets:

• sales.csv – Contains sales transaction details, including sale ID, salesperson ID, sale date, product details, quantity, unit price, and discount. • customers.csv – Contains customer-related information. • products.csv – Contains product details and unit cost information. • targets.csv – Contains salesperson-wise sales targets for different periods.

TOOLS AND TECHNOLOGIES
• Microsoft Power BI – For data visualization and dashboard development. • Power Query – For data cleaning and transformation. • DAX (Data Analysis Expressions) – For creating calculated measures. • CSV Files – For storing and importing the datasets.

KEY PERFORMANCE INDICATORS (KPIs)
The dashboard includes the following key performance indicators:

• Total Sales: Measures the total sales value after applying discounts. • Total Orders: Calculates the number of distinct sales orders. • Total Quantity: Displays the total quantity of products sold. • Total Profit: Calculates profit after deducting product costs. • Total Target: Represents the total sales target. • Achievement Percentage: Measures actual sales as a percentage of the sales target.

DASHBOARD VISUALIZATIONS
The dashboard contains the following visualizations:

• KPI Cards: Display total sales, total orders, total quantity, and total profit. • Monthly Sales Trend: Shows sales performance over time. • Product-Wise Sales Analysis: Compares sales across different products. • Regional Sales Analysis: Displays the contribution of different regions to total sales. • Salesperson Target vs Actual Sales: Compares actual sales against assigned targets for each salesperson. • Interactive Slicers: Allow users to filter the dashboard by region and month.

DATA ANALYSIS AND INSIGHTS
The dashboard helps users understand sales performance across different dimensions.

• Sales Analysis: Total sales are displayed to provide an overview of business revenue. • Order Analysis: Total orders help measure transaction activity. • Quantity Analysis: Total quantity indicates the volume of products sold. • Profit Analysis: Total profit provides an overview of profitability. • Regional Analysis: The regional sales chart helps identify the contribution of each region. • Product Analysis: The product-wise sales chart helps compare product performance. • Target Analysis: The salesperson target vs actual sales chart helps evaluate performance against assigned sales targets.

The displayed KPI values and charts can be used to identify trends and areas that may require improvement.

DAX MEASURES USED
Total Sales = SUMX( sales, sales[quantity] * sales[unit_price] * (1 - sales[discount]) )

Total Quantity = SUM(sales[quantity])

Total Orders = DISTINCTCOUNT(sales[sale_id])

Total Profit = SUMX( sales, sales[quantity] * ( sales[unit_price] * (1 - sales[discount]) - RELATED(products[unit_cost]) ) )

Total Target = SUM(targets[sales_target])

Actual Sales = [Total Sales]

Achievement % = DIVIDE([Actual Sales], [Total Target], 0)

BENEFITS OF THE PROJECT
• Provides a clear overview of sales performance. • Helps monitor business KPIs in one place. • Makes it easier to compare regional and product-wise sales. • Supports salesperson performance evaluation. • Helps identify sales trends and improvement opportunities. • Enables interactive analysis using filters and slicers.

CONCLUSION
The Sales Performance & Target Achievement Dashboard provides an interactive way to analyze business sales data using Microsoft Power BI. It combines important KPIs and visualizations to help users understand sales trends, regional performance, product performance, profitability, and target achievement.

The project demonstrates how data analysis and visualization can convert raw CSV data into meaningful business insights and support informed decision-making.

NOTE: The final analysis should be updated with verified figures from the completed dashboard. Target achievement results should be checked to ensure that salesperson-wise targets are correctly linked to actual sales.
