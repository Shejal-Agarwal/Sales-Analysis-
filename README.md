# Sales-Analysis-Dashboard

### Dashboard Link : [Power BI Dashboard](your-dashboard-link-here)

## Problem Statement

This dashboard helps businesses understand their sales performance better. It enables companies to analyze their product performance, sales trends, and customer behavior across different time periods and geographic locations. Through various metrics and visualizations, businesses can identify top-performing products, optimize discount strategies, and track sales patterns to make data-driven decisions.

The dashboard reveals that Apple iPhone 14 is the leading product with ₹22M in sales and ₹2.25M in profit, while products like Dove Soap Pack and Nivea Body Lotion are underperforming. The analysis of 3,510 orders across 2020-2024 shows steady sales performance with opportunities for growth in emerging markets like Bhopal, Kanpur, and Indore.

Since the profit margin stands at approximately 10% (₹12.9M profit on ₹129M sales), there is significant room for optimization through better product mix, pricing strategies, and targeted promotions.

### Steps followed -

- Step 1 : Load data into Power BI Desktop, dataset is a csv file containing sales transaction data.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that the dataset contains complete information with minimal null values across columns like Customer ID, Order ID, Product ID, Promotion ID, Date, Discount Percentage, Net Sales, Price Per Unit, Profit, Total Sales, and Units Sold.
- Step 5 : In the report view, under the view tab, theme was selected for consistent visualization.
- Step 6 : Visual filters (Slicers) were added for four fields named "Date", "Customer Name", "Product Name" & "Promotion Name" to enable dynamic filtering.
- Step 7 : Multiple card visuals were added to the canvas representing:
   - Total Sales (₹129M)
   - Total Profit (₹12.9M)
   - Total Quantity (7,100+ units)
   - Total Orders (3,510)
   
- Step 8 : Bar charts were added to show Top 5 and Bottom 5 products by:
   - Net Sales
   - Profit
   - Quantity Sold

- Step 9 : A line chart was created to visualize "Sales Trends Over Time" showing monthly sales performance from 2020 to 2024.

- Step 10 : A scatter plot was added to display the "Profit and Net Sales" relationship, helping identify profit optimization opportunities.

- Step 11 : An interactive map visualization was created to show "Sales by City" across major Indian cities including:
   - Bangalore, Visakhapatnam, Kolkata (Top performers)
   - Ahmedabad, Chennai, Delhi (Growing markets)
   - Bhopal, Kanpur, Indore (Emerging markets)

- Step 12 : A bar chart was created to show "Average of Discount by Promotion Name" for:
   - Weekend Flash Sale (23K avg)
   - Clearance Sale (18K avg)
   - Summer Sale (7K avg)
   - New Year Special (3K avg)

- Step 13 : A detailed table was added showing order-level data with columns:
   - Customer ID, Order ID, Product ID, Promotion ID
   - Date, Discount Percentage, Net Sales, Price Per Unit
   - Sum of Profit, Total Sales, Units Sold

- Step 14 : Date comparison filters were implemented allowing users to:
   - Select Date Filter 1 (Start Date to End Date)
   - Select Date Filter 2 (Start Date to End Date)
   - Compare Sales 1 vs Sales 2
   - Compare Profit 1 vs Profit 2
   - Compare Quantity 1 vs Quantity 2

- Step 15 : New measure was created to calculate total sales amount.

Following DAX expression was written:
        
        Total Sales = SUM('Sales Data'[Total Sales])
        
A card visual was used to display total sales.

- Step 16 : New measure was created to calculate total profit.

Following DAX expression was written:
        
        Total Profit = SUM('Sales Data'[Sum of Profit])
        
A card visual was used to display total profit.

- Step 17 : New measure was created to calculate profit margin percentage.

Following DAX expression was written:
        
        Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0) * 100
        
This calculated measure shows the overall profit margin of approximately 10%.

- Step 18 : New measure was created to count total orders.

Following DAX expression was written:
        
        Count of Orders = DISTINCTCOUNT('Sales Data'[Order ID])
        
A card visual was used to display the count of 3,510 orders.

- Step 19 : In the report view, under the insert tab, text boxes were added for dashboard title "SALES ANALYSIS DASHBOARD".

- Step 20 : The report was then published to Power BI Service.

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapshot](your-image-link-here)

# Report Snapshot (Power BI DESKTOP)

![Dashboard_upload](your-image-link-here)

# Insights

A comprehensive multi-page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard:

### [1] Total Sales Performance = ₹129M

   Total Profit = ₹12.9M (10% profit margin)
   
   Total Quantity Sold = 7,100+ units
   
   Total Orders = 3,510

   Analysis Period: January 1, 2020 - December 31, 2024

### [2] Top 5 Products by Net Sales

    a) Apple iPhone 14 - ₹22M
    b) Apple MacBook Air - ₹21M
    c) Sony Bravia 55" TV - ₹21M
    d) Samsung Galaxy S21 - ₹16M
    e) [Product 5] - [Sales Amount]
  
### [3] Top 5 Products by Profit

    a) Apple iPhone 14 - ₹2.25M
    b) Apple MacBook Air - ₹2.08M
    c) Sony Bravia 55" TV - ₹2.05M
    d) [Product 4] - [Profit Amount]
    e) [Product 5] - [Profit Amount]

### [4] Bottom 5 Products by Net Sales

    a) Tupperware Lunch Box - ₹0.28M
    b) L'Oreal Shampoo - ₹0.17M
    c) Nivea Body Lotion - ₹0.09M
    d) Dove Soap Pack - ₹0.09M
    e) [Product 5] - [Sales Amount]
  
### [5] Top 5 Products by Quantity Sold

    a) Apple iPhone 14 - 281 units
    b) Raymond Suit - 274 units
    c) Fossil Smartwatch - 269 units
    d) [Product 4] - [Quantity]
    e) [Product 5] - [Quantity]

### [6] Sales Trends Over Time

    Peak monthly sales: ₹0.65M (Early 2020)
    
    Recent average monthly sales: ₹0.44M - ₹0.52M
    
    Analysis shows relatively steady performance with opportunities for growth initiatives.

### [7] Discount Analysis by Promotion

    a) Weekend Flash Sale - Average discount: 23K
    b) Clearance Sale - Average discount: 18K
    c) Summer Sale - Average discount: 7K
    d) New Year Special - Average discount: 3K
    
Weekend Flash Sale and Clearance Sale are the most aggressive discount promotions.

### [8] Geographic Sales Distribution

Top performing cities:
- Bangalore
- Visakhapatnam
- Kolkata
- Ahmedabad
- Chennai
- Delhi

Emerging markets with growth potential:
- Bhopal
- Kanpur
- Indore
- Lucknow
- Nagpur

### [9] Key Business Insights

9.1) Electronics (iPhone, MacBook, TV) dominate both sales and profit metrics.

9.2) Personal care products (soaps, lotions) show the lowest performance, indicating potential for category optimization.

9.3) The 10% profit margin suggests room for improvement through pricing optimization and cost management.

9.4) Geographic concentration in Bangalore, Visakhapatnam, and Kolkata indicates strong market presence in these cities.

9.5) Steady sales trends over 2020-2024 suggest business stability with opportunities for growth acceleration.

9.6) High discount promotions (Weekend Flash Sale: 23K) may be impacting profit margins and require strategic review.

## Recommendations

1. **Product Strategy**: Focus on high-margin electronics while reconsidering underperforming personal care products.

2. **Geographic Expansion**: Invest in emerging markets (Bhopal, Kanpur, Indore) to diversify revenue sources.

3. **Discount Optimization**: Review Weekend Flash Sale and Clearance Sale strategies to balance volume and profitability.

4. **Profit Margin Improvement**: Target 12-15% profit margin through operational efficiency and pricing strategies.

5. **Trend Analysis**: Leverage period comparison filters to identify seasonal patterns and optimize inventory planning.
