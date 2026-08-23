# Pizza-Sales-Dashboard
# Problem Statement

This dashboard helps a pizza business understand its sales performance so it can make better operational decisions. It shows how much revenue is being generated, how many orders and pizzas are being sold, and which days and hours see the most demand. It also breaks sales down by pizza category and size, and identifies the best and worst selling pizzas helping the business plan staffing, manage inventory, and make informed menu decisions.

Since orders peak on Thursday, Friday and Saturday, and during the 12–1 PM and evening hours, the business should plan extra staffing around these windows. Also, since the Large size and Classic/Supreme categories drive the most revenue, the business can prioritize promoting and stocking these items.

To make sure the numbers shown on the final Excel dashboard are correct and trustworthy, every KPI and chart was first calculated and validated using SQL queries in MS SQL Server, before building the same calculations into the Excel dashboard.

**Part 1 : Data Validation using MS SQL Server**
- Step 1 : Created a new database named `Pizza_DB` in MS SQL Server Management Studio (SSMS).
- Step 2 : Imported the raw `pizza_sales` CSV file (48,620 rows) into the database using Import Flat File, correcting data types where needed (e.g. changing `pizza_id` and `order_id` from Tiny Int to Int since values go beyond single digits).
- Step 3 : Verified the import using `SELECT * FROM pizza_sales;` and confirmed the row count matched the source file (48,620 rows).
- Step 4 : Wrote SQL queries for each KPI and chart requirement, using functions like `SUM, COUNT(DISTINCT ...), CAST, DATENAME,` and `DATEPART.`

**KPI Queries**

**Total Revenue**
<img width="748" height="140" alt="image" src="https://github.com/user-attachments/assets/6446c42b-9dd6-4f8d-96bc-7a1082ba0b3c" />\
<img width="400" height="178" alt="image" src="https://github.com/user-attachments/assets/c3aa5749-3f66-4ef9-9939-1b5ba9268ddc" />

**Average Order Value**
<img width="1270" height="93" alt="image" src="https://github.com/user-attachments/assets/621bec61-33f9-49e1-97ef-6dabe661df27" />
<img width="277" height="157" alt="image" src="https://github.com/user-attachments/assets/232bf447-8075-49e0-9557-2ffc41a5e81d" />

**Total Pizzas Sold**
<img width="821" height="140" alt="image" src="https://github.com/user-attachments/assets/2efcfc7c-c516-4f98-8adf-108e30a68b22" />
<img width="273" height="139" alt="image" src="https://github.com/user-attachments/assets/533459ab-8413-469d-a274-453591a67ff2" />

**Total Orders**
<img width="887" height="112" alt="image" src="https://github.com/user-attachments/assets/b7967fce-f12d-41f9-91d7-78ce2425ec97" />
<img width="310" height="119" alt="image" src="https://github.com/user-attachments/assets/448315ab-e10e-44f7-be41-5615289faa1f" />

**Average Pizzas per Order**
<img width="870" height="78" alt="image" src="https://github.com/user-attachments/assets/5e334dfb-29d9-4aba-b415-21e69acbaa29" />
<img width="273" height="148" alt="image" src="https://github.com/user-attachments/assets/580005a5-2b1f-461d-a79d-71e905ecf1c4" />

#**Trend Queries**

**Daily Trend for Total Orders**
<img width="952" height="81" alt="image" src="https://github.com/user-attachments/assets/bd897b6e-ec73-4a0d-a9d5-8ffb73033340" />
<img width="265" height="270" alt="image" src="https://github.com/user-attachments/assets/d09d9be4-480d-4e0b-a095-f71f8d0eb38a" />

**Hourly Trend for Total Orders**
<img width="982" height="101" alt="image" src="https://github.com/user-attachments/assets/b070d346-176d-487f-9682-1a99c42808fa" />
<img width="273" height="406" alt="image" src="https://github.com/user-attachments/assets/503a21cb-e4d2-46d1-b432-df0394ecf4eb" />

#**Sales Breakdown Queries**

**% of Sales by Pizza Category**
<img width="1263" height="171" alt="image" src="https://github.com/user-attachments/assets/9c71b960-a5cb-40a7-a58e-b64f7f15e716" />
<img width="329" height="189" alt="image" src="https://github.com/user-attachments/assets/3ca95061-da82-48d5-b577-148dc0efae51" />


**% of Sales by Pizza Size**
<img width="1245" height="153" alt="image" src="https://github.com/user-attachments/assets/5a7e5f2d-7824-4172-8f45-b3d7550c04ff" />
<img width="317" height="210" alt="image" src="https://github.com/user-attachments/assets/b0c0df53-f4fc-4e12-bc3f-183d42f7224e" />

**Total Pizzas Sold by Category**
<img width="675" height="116" alt="image" src="https://github.com/user-attachments/assets/23fa96f2-f060-4aa0-b986-7ac514e0b173" />
<img width="273" height="176" alt="image" src="https://github.com/user-attachments/assets/f9659158-f711-428b-aef2-5057193a1058" />

#**Best & Worst Sellers Queries**

**Top 5 Best Sellers by Total Pizzas Sold**
<img width="717" height="127" alt="image" src="https://github.com/user-attachments/assets/fc8b2768-a956-474f-afa2-def0dedc28be" />
<img width="336" height="188" alt="image" src="https://github.com/user-attachments/assets/09d970a8-453a-4d6a-89af-e8bbbb3e4b05" />

**Bottom 5 Worst Sellers by Total Pizzas Sold**
<img width="651" height="110" alt="image" src="https://github.com/user-attachments/assets/7bbf322c-a38f-4456-ac30-e3f376d2b2ab" />
<img width="336" height="205" alt="image" src="https://github.com/user-attachments/assets/ad3706ee-ccb6-4247-9cdd-9740d6d20a2d" />


#**Part 2 : Dashboard built in Excel**
- Step 1 : Loaded the cleaned pizza sales dataset into Excel (either connected directly to the SQL Server database, or used the flat CSV file).
- Step 2 : Cleaned the data — corrected the pizza size labels (S, M, L → Small, Medium, Large) and formatted date/time columns correctly.
- Step 3 : Built the same KPI calculations validated in SQL, using Excel formulas `(SUM, COUNTA/COUNT, AVERAGE, SUMPRODUCT for distinct counts).`
- Step 4 : Created a Daily Trend chart and an Hourly Trend chart for Total Orders using PivotTables/PivotCharts.
- Step 5 : Created a donut chart for % of Sales by Pizza Category and a pie chart for % of Sales by Pizza Size.
- Step 6 : Built a Top 5 Best Sellers chart and a Bottom 5 Worst Sellers chart, ranking pizzas by total quantity sold.
- Step 7 : Added a Month slicer/timeline so the dashboard can be filtered to show data for any specific month.
- Step 8 : Arranged all KPI cards, charts, and slicers onto a single Dashboard sheet, using a dark theme with a pizza-themed header image and consistent color coding across visuals.
- Step 9 : Compared every KPI and chart value against the SQL query results from Part 1 to confirm the dashboard is showing accurate numbers.


<img width="997" height="532" alt="image" src="https://github.com/user-attachments/assets/09afc895-bc3f-4322-ab8c-3c5459903086" />


**Insights**

A single page interactive dashboard was built in Excel using KPI cards, charts, and slicers.

Following inferences can be drawn from the dashboard:

**[1] Overall KPIs**
- Total Revenue = $817,860.05
- Average Order Value = $38.31
- Total Pizzas Sold = 49,574
- Total Orders = 21,350
- Average Pizzas per Order = 2.32

  <img width="929" height="96" alt="image" src="https://github.com/user-attachments/assets/a0527ef3-fd77-4025-aa23-e5f4a4c83134" />

  
**[2] Daily Trend**
- Highest orders occur on Friday (330), Thursday (329) and Saturday (303).
- Lowest orders occur on Sunday (199). thus, the business should plan extra staffing on Thursday – Saturday.
  
**[3] Hourly Trend**
- Orders peak between 12–1 PM (lunch) and again in the evening hours. thus, staffing should be scaled up around these hours.
  
**[4] Sales by Category**
- Sales are fairly evenly spread across the four categories Chicken, Classic, Supreme and Veggie each contributing roughly 21–30% of total sales, with the Classic category contributing the most.

**[5] Sales by Size**
-Large pizzas contribute the most to sales (38.15%), followed by Small (31.31%) and Medium (29.26%).
- X-Large (1.17%) and XX-Large (0.11%) make up a very small share of sales. thus, Large size drives maximum revenue and should be prioritized in promotions.
  
**[6] Best & Worst Sellers**
- **Best sellers (by quantity sold):** The Pepperoni Pizza, The Barbecue Chicken Pizza, The California Chicken Pizza, The Thai Chicken Pizza, The Sicilian Pizza.
- **Worst sellers (by quantity sold):** The Spinach Pesto Pizza, The Chicken Pesto Pizza, The Green Garden Pizza, The Mediterranean Pizza, The Calabrese Pizza, and lowest of all The Brie Carre Pizza. thus, the business could promote the top sellers further and consider reworking or removing the lowest performers from the menu.
