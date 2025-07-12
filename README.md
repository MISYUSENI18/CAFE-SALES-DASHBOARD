# CAFE-SALES-DASHBOARD
## Café Sales Dashboard Project
This project explores and analyzes 10,000+ café sales records using Excel and Power Query. It includes data cleaning, KPIs, business insights, and a visual dashboard.
CAFÉ SALES DASHBOARD
#### Project Title: Dirty Café Sales Dataset
#### Introduction:
This analysis examines the performance of sales transactions in a café. The goal is to uncover insights and provide actionable recommendations that will improve customer service and overall sales performance.
#### Problem Statement:
The café lacks visibility into its sales trends, customer preferences, and payment behaviors, making it difficult to strategize for growth and operational improvement.
#### Objectives:
•	Examine the performance of sales.
•	Identify top-selling items, trends, and customer behaviors.
•	Suggest strategies to improve services and boost sales.
### METHODOLOGY
#### Excel:
Used to create visualizations, such as:
•	Bar charts, column charts, line charts, scatter plots, and treemaps.
•	KPI cards and dashboard layout to communicate insights.
Power Query (inside Excel):
•	Loaded the dirty dataset
•	Transformed and cleaned the data:
o	Extracted Day, Month, and Year from the Transaction Date
o	Handled null, missing, and inconsistent values
•	Close & Load back into Excel for final dashboard build
#### DATA TRANSFORMATION
Extract, Load, and Transform (ELT):
#### Dataset Size: 10,000 rows of synthetic, intentionally messy café sales data
#### Data Structure:
•	Transaction ID: Unique identifier
•	Item: Item sold (Coffee, Cake, etc.)
•	Payment Method: e.g., Cash, Card, Wallet
•	Location: Where the purchase was made
•	Transaction Date
•	Quantity
•	Price Per Unit
•	Total Spent
#### Cleaning & Transformation Steps:
1. Handling Duplicates
•	Checked all rows for duplicate entries → None found
2. Handling Missing Values
•	Added custom logic in Power Query:
“= if [Total Spent] = null and [Quantity] <> null and [Price Per Unit] <> null then [Quantity] * [Price Per Unit] else [Total Spent]”
•	Similar logic applied for calculating missing Quantity or Price Per Unit
•	Cells showing “ERROR” or “UNKNOWN” were replaced with “null” across all columns
•	Entire Transaction column was dropped due to irrelevance or corruption
3. Standardizing Data
•	Categorical values cleaned (e.g., "Digital Wallet", not "wallet" or "e-wallet")
•	Proper formatting applied to numeric, currency, and date columns
•	Data types for each column were checked and corrected to the appropriate format:
o	Quantity → Whole Number
o	Price Per Unit → Decimal
o	Total Spent → Currency
o	Transaction Date → Date
•	Transaction Date column was parsed into Day, Month, and Year components
 #### Final Load & Dashboard:
•	A slicer for Days of the Week was added to improve interactivity and allow users to filter sales performance by weekday. This helps identify which days generate the most revenue and inform staffing or promotional decisions.
•	Cleaned data reviewed for accuracy and completeness
•	Dashboard created in Excel:
o	KPI Cards: Total Revenue, Total Quantity, Average Price per Unit
o	Charts: Monthly Trends, Top Payment Method, Most Ordered Items, Revenue by Item
o	Color-coded, structured layout, and text-enhanced visuals
#### KPI OVERVIEW
##### Key KPIs:
•	Total Revenue: Measures overall income generated from sales.
•	Total Quantity Sold: Tracks the number of items sold.
•	Average Price per Unit: Indicates the average cost of each item sold.
These KPIs provide a snapshot of the business’s financial health and performance trends.

#### KEY BUSINESS QUESTIONS
1.	On which day of the week does the café see the highest sales volume?
2.	What are the revenue trends across different months?
3.	Which item generates the highest revenue?
4.	Which payment method is most popular among customers?
5.	Which month had the highest average revenue?
6.	What is the overall sales performance?
#### INSIGHTS
•	Salad recorded the highest revenue, suggesting it's a strong performer worth continued focus.
•	Digital Wallet is the most used payment method, highlighting the importance of maintaining and promoting digital payment options.
•	April had the highest monthly average revenue, possibly due to seasonal effects or promotions.
•	Total revenue surpassed $88,000 with 30,000+ items sold, indicating a healthy volume of sales.
•	Items like Tea and Water are high in quantity but low in revenue, signaling potential for upselling or pricing strategy adjustments.
#### RECOMMENDATIONS
•	Ensure complete and accurate data entry: Several records had only one of the three core financial columns filled (e.g., only Quantity, or only Price Per Unit), which made it impossible to compute the missing values. Staff should be trained to ensure every transaction has all necessary fields recorded correctly: Quantity, Price Per Unit, and Total Spent.
•	Continue promoting top-selling items like Salad, while exploring bundled offers or loyalty rewards to encourage repeat purchases.
•	Reevaluate low-revenue items to determine if price adjustments or packaging could improve profitability.
•	Leverage Digital Wallets by offering incentives or faster checkout options, as they are the preferred payment method.
•	Investigate the success in April to identify any repeatable campaigns, promotions, or seasonal trends that can be capitalized on in future months.


