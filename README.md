<img src="/Images/bg.jpg" width="600" height="340"/>
<h1>Global Superstore Sales Report</h1>
<h2>Project Overview:</h2>
<p>This project focuses on the in-depth analysis of Superstore data to uncover actionable insights and drive data-informed decision-making. 
By exploring key performance metrics and trends, the goal is to identify growth opportunities, optimize processes, and enhance overall business performance.</p>
<h2>Key Objective:</h2>
<p>Analyze monthly, quarterly, and yearly trends for Revenue and Total Orders to identify seasonality, growth patterns, and other time-related insights.</p>
<p>Explore Category, Subcategory, and Product-wise contributions to Revenue.</p>
<p>Explore region-wise, country-wise, and market-wise patterns and trends to understand geographic variations in performance.</p>
<p>Calculate and analyze YoY percentage growth for Orders, Profit, and Revenue.</p>
<h2>Data Preparation Phase:</h2>
<p>The Excel file contained two sheets: Orders and Returns. First, I accessed both data tables using pandas and began by exploring each column in detail. This involved identifying the number of non-null and unique values, as well as checking the data type of each column.</p>
<p float="left"><img src="/Images/pandas1.jpg" width="400" height="150"/>&nbsp;&nbsp;<img src="/Images/pandas2.jpg" width="400" height="150"/></p>
<p>The Postal Code column had only 19.48% non-null values, so I decided to drop it. Since both the Order Date and Ship Date columns contained only date values, I adjusted their data types from datetime to date. I repeated the same process for the Returns table to ensure consistency.</p>
<p>Finally, I exported the both the transformed tables from pandas back into an Excel file and imported it into Power BI for further analysis.</p>
<h2>Data Modelling Phase:</h2>
<img src="/Images/model.jpg" width="500" height="200"/>
<p>After importing both files separately into Power BI, I performed initial operations such as renaming tables and adjusting column data types before loading the data into the semantic model. </p>
<p>After loading, I created a relationship between the Returns and Orders tables using the common column ‘Order ID,’ setting cardinality to One-to-Many and cross-filtering direction to ‘Both.’</p>
<p>I created a calculated table named Calendar using the CALENDARAUTO() function, adding columns like year, month, quarter, etc. Then, I joined the Orders table to the Calendar table using the common column ‘Order Date.’</p>
<p>I created multiple measures to summarize and aggregate data in the desired manner.
Some key metrics included in this report are: Total Revenue, Total Orders, Total Quantity Sold, Profit Margin, Average bucket size, Average bill size, YOY growth in revenue, profit, orders, and returns, Shipping cost per order, etc.</p>
<p>I also created various hierarchies to enable drill-down functionality in visuals. These hierarchies are Date Hierarchy (Year-Quarter-Month), Market Hierarchy (Market-Region-Country-City), and Category Hierarchy (Category-Subcategory-Product).</p>
<h2>Data Visualization Phase:</h2>
<p>In the report, I included three pages: Sales Overview, Market-wise Report, and Category-wise Report. The Market-wise Report and Category-wise Report are drill-through pages.</p>
<img src="/Images/overview.jpg" width="600" height="340"/>
<p>On the first page, Sales Overview, an overview of sales performance is provided through various visuals that showcase different aspects of store performance in a visually appealing manner. These visuals include:</p>
<ol>
  <li>Line & Column chart illustrating Yearly, Monthly, and Quarterly trends of Revenue and Orders over time.</li>
  <li>Bar charts comparing Revenue by Segments, Categories, and Markets.</li>
  <li>KPI visuals displaying YOY growth for Revenue, Profit, Orders, and Returns.</li>
  <li>Cards presenting Total Revenue, Profit Margin, and Total Returns.</li>
  <li>A Donut chart comparing Orders by Ship Mode.</li>
</ol>
<p>In addition to this high-level overview, users are given the option to drill through into each market and category for more detailed insights.</p>
<p float="left"><img src="/Images/drillthrough1.jpg" width="480" height="320"/>&nbsp;&nbsp;&nbsp;<img src="/Images/drillthrough2.jpg" width="480" height="320"/></p>
<p>The two drill-through pages consist of: <b>Market-wise Report:</b> This page features a matrix visual that provides a detailed tabular representation, showcasing various attributes such as Revenue, Orders, Profit Margin, Revenue per Store, and more across each Region, Country, and City in the selected market.</p>
<p><b>Category-wise Report:</b> Similar to the Market-wise Report, this page offers a detailed tabular representation across each Subcategory and Product within the selected category.</p>
<h2>Insights:</h2>
<p>Revenue and Orders have shown steady growth from 2012 to 2015.</p>
<p>Asia Pacific and Europe are the leading markets in terms of revenue generation. The highest revenue comes from the Technology Category. Among customer segments, Consumer contributes the most to Total Revenue.</p>
<p>The United States is the highest revenue-generating country, and the product generating the most revenue is ‘Tech-Ph-3148.’</p>
<p>he most preferred ship mode is Standard Class, which accounts for 59.84% of total orders. However, for critical orders, customers tend to prefer First Class Ship Mode.</p>
<h2>Trends & Patterns:</h2>
<p>A commonly observed trend in orders and revenue is that both show a drop in the first quarter and then experience steady growth for the rest of the quarters.</p>
<p>Revenue, Orders, and Profits are displaying strong YOY percentage growth of 26.25%, 28.68%, and 23.89%, respectively. However, the number of returns has also increased by 28.92%. While this increase aligns proportionally with order growth and is understandable, it requires attention. Efforts should be made to address customer complaints to identify the root causes of the returns.</p>
<p>In the Furniture category, the YOY growth in returns is significantly higher than the YOY growth in orders, which is alarming. Within the Furniture category, Furnishings and Bookcases require immediate attention as returns are showing annual growth rates of 65.38% and 53.85%, respectively.</p>
<p>Avoid aggressive discounting. When discounts are between 0% and 20%, the average profit margin achieved is 21%. However, when discounts exceed 20%, the profit margin turns negative. Maintaining a balanced approach to discounting is crucial. Focus discounts in areas where market penetration is still low.</p>
<p>For instance, the African market generates the least revenue overall. However, this year, it has shown significant growth in orders, revenue, and profit. Using discounting strategically in Africa to expand the customer base can be a viable approach.</p>












