[README.md](https://github.com/user-attachments/files/34296859/README.md)
# E-Commerce Sales & Profitability Analysis

An Excel-based data analytics project focused on understanding sales performance, product profitability, customer behaviour, and regional business performance.

## Project Overview

For this project, I worked with an e-commerce sales dataset covering one complete financial year, from April 2025 to March 2026.

The main objective was to understand how the business was performing beyond just its sales numbers. I explored which products and categories generated the most profit, how discounts related to profitability, which customer segments contributed the most, and how performance varied across regions.

I completed the analysis using Microsoft Excel, Power Query, Power Pivot, PivotTables, and DAX. I also created three dashboards to present the findings clearly.

## Business Problem

An e-commerce business may generate good sales but still struggle to maintain profitability because of discounts, product costs, shipping expenses, marketplace fees, and product returns.

This project explores questions such as:

- Which months generate the highest and lowest sales?
- Which product categories contribute the most to revenue and profit?
- Are higher discounts associated with lower profit margins?
- Which products generate the highest profit?
- Which customer segments contribute the most?
- Which states perform best in sales and profitability?
- Which products have comparatively higher returned quantities?

The aim was to turn raw sales data into useful business insights that could support better decision-making.

## Dataset Overview

The dataset is synthetic and represents an Indian e-commerce business.

- **Total records:** Approximately 4,000
- **Total columns:** 22
- **Reporting period:** April 2025 – March 2026
- **Data format:** TXT files
- **Source files:** 16 batches
- **Country context:** India

The dataset includes order, customer, product, sales, cost, payment, shipping, and return information.

Important columns include:

- Order details: `Order_ID`, `Order_Date`, `Order_Status`
- Customer details: `Customer_ID`, `Customer_Name`, `City`, `State`, `Customer_Segment`
- Product details: `Product_ID`, `Product_Name`, `Category`, `Subcategory`
- Sales details: `Quantity`, `Unit_Price`, `Discount_Pct`
- Cost details: `Unit_Cost`, `Shipping_Cost`, `Marketplace_Fee_Pct`
- Other details: `Sales_Channel`, `Payment_Method`, `Return_Flag`, `Return_Date`

## Tools & Technologies Used

- **Microsoft Excel:** Data analysis, PivotTables, dashboards, and reporting.
- **Power Query:** Importing, combining, cleaning, and transforming TXT files.
- **Power Pivot:** Creating relationships and managing the Data Model.
- **DAX:** Creating measures for sales, costs, profit, margins, and returns.
- **PivotTables and PivotCharts:** Summarizing data and building visualizations.
- **GitHub:** Project documentation and portfolio presentation.

## Data Preparation

The original dataset was provided in 16 separate TXT files. Instead of importing each file individually, I used Power Query to combine them into one dataset.

The main preparation steps were:

1. Imported and combined all 16 TXT files using Power Query.
2. Created a consolidated query named `Raw_AllBatches`.
3. Created a referenced query named `Clean_Sales` for cleaning and transformation.
4. Checked missing values, data types, and errors.
5. Created separate Product and Customer dimension tables.
6. Created a Calendar table covering the complete reporting period.
7. Loaded the cleaned tables into the Excel Data Model.

## Data Model

I used a Star Schema to organize the data and make analysis easier.

The model contains one fact table and three dimension tables:

- **Clean_Sales:** Main sales transaction table.
- **Product:** Product and category information.
- **Customer:** Customer and regional information.
- **Calendar:** Date-related information.

### Relationships

- `Calendar[Date]` → `Clean_Sales[Order_Date]`
- `Product[Product_ID]` → `Clean_Sales[Product_ID]`
- `Customer[Customer_ID]` → `Clean_Sales[Customer_ID]`

This structure helped me analyze sales across different dimensions without repeatedly combining the same information.

## Key DAX Measures

I created DAX measures to calculate the main business metrics:

- **Gross Sales:** Sales before discounts.
- **Discount Amount:** Total discount provided.
- **Net Sales:** Sales after discounts.
- **Total Orders:** Distinct count of orders.
- **Total Quantity:** Total units sold.
- **Average Order Value:** Average sales value per order.
- **Total Product Cost:** Total product purchase cost.
- **Total Shipping Cost:** Total shipping expenses.
- **Total Marketplace Fees:** Marketplace-related fees.
- **Total Profit:** Profit after the calculated costs.
- **Profit Margin %:** Profit as a percentage of net sales.
- **Average Discount %:** Average discount percentage.
- **Returned Orders:** Number of orders with returned items.
- **Return Rate %:** Returned orders as a percentage of total orders.
- **Returned Quantity:** Total quantity marked as returned.

## Dashboard Overview

I created three separate dashboards to explore different areas of the business.

### 1. Executive Dashboard

This dashboard provides an overall view of business performance.

**Key KPIs:**

- Net Sales
- Total Profit
- Profit Margin
- Total Orders
- Average Order Value
- Return Rate

**Visualizations:**

- Monthly Net Sales Trend
- Monthly Profit Trend
- Category-wise Sales & Profit
- Sales Channel Performance
- Top 5 States by Net Sales

### 2. Product Dashboard

This dashboard focuses on product performance, profitability, and cost-related analysis.

**Visualizations:**

- Top 10 Products by Net Sales
- Top 10 Products by Total Profit
- Category-wise Profit Margin Analysis
- Discount Impact on Profitability
- Product-wise Return Analysis
- Cost Breakdown Analysis

### 3. Customer & Regional Dashboard

This dashboard focuses on customer segments and regional business performance.

**Visualizations:**

- Customer Segment Sales Analysis
- Customer Segment Profitability
- Top 10 Customers by Net Sales
- Average Order Value by Customer Segment
- State-wise Sales Performance
- City-wise Sales Contribution
- Regional Profitability Analysis

## Dashboard Interactivity

I added slicers to make the dashboards easier to explore:

- Calendar Year
- Calendar Month
- Product Category
- Customer State
- Sales Channel
- Customer Segment

These slicers allow users to filter the dashboards by time period, category, region, sales channel, and customer segment.

## Key Business Insights

After analyzing the dataset, I identified the following findings:

1. **Monthly Sales Performance:** April recorded the highest net sales of ₹4,90,544.21, followed by May with ₹4,55,488.85. August recorded the lowest net sales of ₹1,07,449.55, showing considerable variation in monthly sales.

2. **Product & Category Profitability:** Electronics generated the highest net sales of ₹15,54,905.26 and total profit of ₹4,06,594.75. However, Accessories achieved the highest profit margin of 46.69%, showing that the category with the highest revenue does not necessarily have the highest profit margin.

3. **Discount & Profitability:** Higher discount rates did not consistently correspond to lower profit margins across the selected products. Products with similar discount percentages showed different profitability levels, indicating that product pricing and costs also play a role.

4. **Customer & Regional Performance:** Corporate customers generated the highest net sales of ₹13,72,317.49, total profit of ₹3,60,481.13, and average order value of ₹6,861.59. Gujarat recorded the highest net sales of ₹4,47,232.71, while Karnataka generated the highest total profit of ₹1,29,769.47.

5. **Product Returns:** Running Sports Shoes recorded the highest returned quantity, with 8 units, among the products included in the return analysis.

## Business Recommendations

Based on the findings, I would suggest the following actions:

1. **Optimize Discount Strategies:** Review discount policies across product categories. Fashion offers the highest average discount of 15.81% while maintaining a profit margin of 39.71%. Discount decisions should consider product-level profitability rather than relying on a uniform strategy.

2. **Focus on Profitable Products:** Noise Cancelling Headphones generated ₹88,619.81 in total profit among the five leading products. The business could prioritize promoting high-profit products while reviewing the pricing and costs of relatively lower-profit products.

3. **Strengthen Customer Relationships:** The Corporate segment contributes the highest sales, profit, and average order value. Personalized offers and loyalty programs could help strengthen relationships with these customers.

4. **Improve Regional Profitability:** Gujarat leads in net sales, while Karnataka leads in total profit. Studying the factors behind Karnataka's profitability could help identify strategies worth applying in other regions.

5. **Reduce Product Returns:** Running Sports Shoes has the highest returned quantity in the analyzed product list. Investigating sizing, product quality, product descriptions, and delivery issues could help reduce avoidable returns.

## Limitations & Assumptions

There are a few assumptions and limitations to consider when interpreting the results:

- The dataset is synthetic and does not represent actual company transactions.
- `Unit_Cost` is treated as the cost per individual product unit.
- `Shipping_Cost` is summed at the transaction-line level. This assumes it is not duplicated across multiple product lines of the same order.
- Marketplace fees are calculated on discounted net sales.
- Profit calculations are based on the available cost fields and do not fully account for refunds or returned-product adjustments.
- Some records contain missing values, including return dates and marketplace fee percentages. These require careful interpretation rather than automatically treating missing values as zero.
- The calculated profit should therefore be treated as an analytical estimate under the stated assumptions, not necessarily final realized business profit.

## Project Files

The project contains the following main deliverables:

- **E-Commerce Sales & Profitability Analysis.xlsx:** Main Excel workbook containing the Data Model, Power Query transformations, DAX measures, PivotTables, and interactive dashboards.
- **Executive Dashboard PDF:** A3-size exported dashboard showing overall business performance.
- **Product Dashboard PDF:** A3-size exported dashboard showing product and profitability analysis.
- **Customer & Regional Dashboard PDF:** A3-size exported dashboard showing customer and regional performance.
- **README.md:** Project documentation.

## Conclusion

This project gave me practical experience in working with raw data and turning it into meaningful business information using Excel.

While building it, I worked with Power Query for data cleaning, Power Pivot for data modelling, DAX for calculations, and PivotTables and PivotCharts for analysis and visualization.

More importantly, I learned that looking only at revenue does not give a complete picture of business performance. Understanding profit margins, discounts, operating costs, customer segments, and returns is equally important.

This project is one of my steps towards developing practical data analytics skills and building a portfolio based on analytical workflows.

---

**Project:** E-Commerce Sales & Profitability Analysis  
**Tools:** Microsoft Excel | Power Query | Power Pivot | DAX  
**Reporting Period:** April 2025 – March 2026
