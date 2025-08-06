# 🛒 Online Retail Power BI Dashboard

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

## 📊 Key Insights

- 📈 **Consistent sales growth** observed across months, peaking in Q4.
- 🏆 **Top-selling product category** dynamically calculated using DAX.
- 📍 **Customer distribution** is concentrated in key Nigerian cities.
- 🧠 **KPIs** like Total Sales, Average Order Value, and Order Volume are visualized clearly for business impact.

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

This project has deepened my confidence in connecting SQL with business intelligence tools, and it stands as a testament to my ability to turn complex data into decisions. As I continue to grow in this field, I’m excited to keep exploring ways to turn raw numbers into compelling stories.

## License
This project is licensed under the MIT License.

## 🔗 Author
Built by Chidiogor Nwafor
 
Built by **Chidiogor Nwafor**  
[🔗 LinkedIn](https://www.linkedin.com/in/chidiogor-nwafor) | [📂 Portfolio](#) | [✍️ Medium](https://medium.com/@your-medium-username) | [ GitHub](https://github.com/diogor1)
