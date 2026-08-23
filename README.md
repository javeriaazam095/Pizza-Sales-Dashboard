# Pizza-Sales-Dashboard
# Problem Statement

This dashboard helps a pizza business understand its sales performance so it can make better operational decisions. It shows how much revenue is being generated, how many orders and pizzas are being sold, and which days and hours see the most demand. It also breaks sales down by pizza category and size, and identifies the best and worst selling pizzas helping the business plan staffing, manage inventory, and make informed menu decisions.

Since orders peak on Thursday, Friday and Saturday, and during the 12–1 PM and evening hours, the business should plan extra staffing around these windows. Also, since the Large size and Classic/Supreme categories drive the most revenue, the business can prioritize promoting and stocking these items.

**Steps followed**
- Step 1 : Loaded the raw pizza sales dataset (order level data with pizza name, category, size, quantity, price, order date and time) into Excel.
- Step 2 : Cleaned the data checked for missing values, corrected the pizza size labels (S, M, L → Small, Medium, Large), and formatted date/time columns correctly.
- Step 3 : Built a set of KPI calculations using formulas (SUM, COUNT, AVERAGE, DISTINCT COUNT) to summarize the dataset:
**Total Revenue**
- Average Order Value
- Total Pizzas Sold
- Total Orders
**Average Pizzas per Order**
- Step 4 : Created a Daily Trend chart for Total Orders using DATENAME(WEEKDAY, order_date) style grouping, to see which days of the week get the most orders.
- Step 5 : Created an Hourly Trend chart for Total Orders, grouping orders by the hour extracted from order time, to see peak ordering hours.
- Step 6 : Calculated % of Sales by Pizza Category using the formula: '(Category Sales ÷ Total Sales) × 100', and represented it with a donut chart.
- Step 7 : Calculated % of Sales by Pizza Size using the same percentage logic, and represented it with a pie chart.
- Step 8 : Built a Top 5 Best Sellers chart and a Bottom 5 Worst Sellers chart, ranking pizzas by total quantity sold (ORDER BY descending / ascending).
- Step 9 : Added a Month slicer/timeline so the dashboard can be filtered to show data for any specific month.
- Step 10 : Arranged all KPI cards, charts, and slicers onto a single Dashboard sheet, using a dark theme with a pizza themed header image and consistent color coding across visuals.
- Step 11 : Tested the slicer and chart interactivity to make sure all visuals update correctly when filtered.


**Insights**

A single page interactive dashboard was built in Excel using KPI cards, charts, and slicers.

Following inferences can be drawn from the dashboard:

**[1] Overall KPIs**
- Total Revenue = $817,860.05
- Average Order Value = $38.31
- Total Pizzas Sold = 49,574
- Total Orders = 21,350
- Average Pizzas per Order = 2.32
**[2] Daily Trend**
- Highest orders occur on Friday (330), Thursday (329) and Saturday (303).
- Lowest orders occur on Sunday (199). thus, the business should plan extra staffing on Thursday – Saturday.
**[3] Hourly Trend**
- Orders peak between 12–1 PM (lunch) and again in the evening hours. thus, staffing should be scaled up around these hours.
**[4] Sales by Category**
- Sales are fairly evenly spread across the four categories — Chicken, Classic, Supreme and Veggie — each contributing roughly 21–30% of total sales, with the Classic category contributing the most.
**[5] Sales by Size**
-Large pizzas contribute the most to sales (38.15%), followed by Small (31.31%) and Medium (29.26%).
- X-Large (1.17%) and XX-Large (0.11%) make up a very small share of sales. thus, Large size drives maximum revenue and should be prioritized in promotions.
**[6] Best & Worst Sellers**
- **Best sellers (by quantity sold):** The Pepperoni Pizza, The Barbecue Chicken Pizza, The California Chicken Pizza, The Thai Chicken Pizza, The Sicilian Pizza.
- **Worst sellers (by quantity sold):** The Spinach Pesto Pizza, The Chicken Pesto Pizza, The Green Garden Pizza, The Mediterranean Pizza, The Calabrese Pizza, and lowest of all The Brie Carre Pizza. thus, the business could promote the top sellers further and consider reworking or removing the lowest performers from the menu.
