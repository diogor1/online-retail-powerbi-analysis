# Online Retail Power BI Dashboard

An interactive Power BI dashboard that analyzes retail store data, uncovering patterns in sales, customer orders, and product categories. Built using real-world data structured in SQL and connected directly to Power BI.

![Dashboard Screenshot](![online retail bisql](https://github.com/user-attachments/assets/8a54f5fd-41d6-4af6-8629-3843345be5e4)
)

---

## 📌 Project Overview

This project is part of a full-stack data analytics journey using:
- Microsoft SQL Server (data storage)
- Power BI (data modeling and visualization)
- DAX (for calculated metrics and KPIs)

The dashboard provides a real-time view of:
- Total sales & orders
- Top product categories
- Sales trends over time
- Geographic distribution of customers

---

## ⚙️ Tools Used

- **Power BI Desktop**
- **SQL Server (Microsoft SQL)**
- **DAX (Data Analysis Expressions)**
- **Power Query Editor**

---

## Key Insights
1. Consistent Revenue Growth Over Time
The line chart reveals a steady upward trend in revenue, with notable spikes during certain months. This suggests the business experiences periodic boosts in customer activity, potentially linked to promotions or seasonal demand. These patterns are crucial for forecasting and strategic planning.

2. Top-Selling Product Categories Identified Dynamically
Using a DAX-driven measure, the dashboard pinpoints the highest-performing product category in real time. This empowers decision-makers to focus inventory, marketing, and investment efforts on products that generate the most revenue.

3. Geographic Concentration of Customers
The location map shows that most purchases are clustered in key Nigerian cities like Lagos, Abuja, and Ibadan. This insight helps in targeting regional campaigns, optimizing logistics, and understanding geographic demand patterns.

4. Comprehensive KPI Overview
Core metrics like Total Sales, Order Count, Total Quantity Sold, and Average Order Value are presented in KPI cards. These indicators provide a quick snapshot of business health and allow stakeholders to assess performance at a glance.

5. Interactivity and Drill-Down Capabilities
Slicers and date hierarchies allow users to explore the data by category, location, and time, promoting deeper insight without overwhelming the dashboard. This level of interactivity enhances usability, especially for non-technical stakeholders.



---

##  Dynamic DAX Measures

```DAX
Total Sales = SUMX(order_items, order_items.Quantity * order_items.UnitPrice)

Top Category = 
VAR CategorySales =
    SUMMARIZE(
        products,
        products[category],
        "TotalSales", CALCULATE(SUM(order_items[sales]))
    )
RETURN
    MAXX(
        TOPN(1, CategorySales, [TotalSales], DESC),
        products[category]
    )
```

##  Final Thoughts
This Power BI dashboard represents more than just visual analytics; it marks a key milestone in my journey as a data analyst. From raw SQL data to interactive storytelling, I set out to build a project that not only showcases technical skills but also delivers meaningful insights that business stakeholders can act on.

Throughout this process, I practiced end-to-end analysis:

Extracting and cleaning data using SQL

Creating calculated measures and relationships in Power BI

Designing visuals that emphasize clarity, interactivity, and impact

One of the most fulfilling moments was watching the data come alive, revealing trends in product categories, order behaviors, and customer locations. Even better, I was able to dynamically calculate top-performing categories using DAX, a feature that would be valuable in any retail business scenario.



## License
This project is licensed under the MIT License.

## 🔗 Author
Built by Chidiogor Nwafor
 
Built by **Chidiogor Nwafor**  
[🔗 LinkedIn](https://www.linkedin.com/in/chidiogor-nwafor) | [📂 Portfolio](#) | [✍️ Medium](https://medium.com/@your-medium-username) | [ GitHub](https://github.com/diogor1)
