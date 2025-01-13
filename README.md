# Maven Market Dashboard Analysis

## **Project Overview**

This project presents a detailed analysis of the **Maven Market dataset**, containing retail sales information. The goal of this analysis is to examine and present insights into the top-line performance of the business, specifically focusing on the years **1997** and **1998**. The analysis utilizes **Power BI** and **DAX** to build an interactive dashboard that identifies business trends, evaluates performance, and aids in making informed decisions.

### **Dataset Used**
The dataset used for this analysis is the **Maven Market dataset**, which includes sales data for various products, customers, stores, and regions.

### **Goal of the Analysis**
The primary objectives of this project are:
- Analyze **top-line performance** for 1997 and 1998.
- Understand key metrics such as **total revenue**, **total profit**, **sales trends**, and **customer behavior**.
- Present insights through various visualizations to inform business decision-making.

---

## **Agenda**

1. [Key Metrics & Insights](#key-metrics--insights)
2. [Data Source](#data-source)
3. [Technologies Used](#technologies-used)
4. [Visualizations](#visualizations)
5. [Data Cleaning & Transformation](#data-cleaning--transformation)
6. [Data Modeling](#data-modeling)
7. [Challenges Faced](#challenges-faced)
8. [Key Takeaways](#key-takeaways)
9. [Next Steps](#next-steps)
10. [Dashboard Pages](#dashboard-pages)

---

## **Key Metrics & Insights**

### **KPIs & Metrics**

Several KPIs and metrics were analyzed, including:

- **Total Revenue**: Measures the total revenue generated from all transactions.
- **Total Profit**: Represents the total profit made from all transactions.
- **Return Rate**: The percentage of products returned by customers.
- **Average Order Value (AOV)**: Represents the average amount spent per order.
- **Sales Growth**: Measures the percentage change in revenue over time.
- **Revenue by Product Category**: Breaks down the total revenue by product category to assess profitability.

### **Main Findings**
- **Revenue Trends**: Fluctuations in revenue were observed in both 1997 and 1998. These fluctuations highlight peak sales periods and varying product performance.
- **Product Performance**: Certain product brands performed significantly better, helping to guide inventory and marketing decisions.
- **Return Rates**: Some products had high return rates, potentially signaling customer dissatisfaction or product quality issues.
- **Customer Behavior**: Repeat purchases were more common within certain customer segments, suggesting areas for targeted marketing efforts.

---

## **Data Source**

- **Source**: The **Maven Market dataset** is publicly available and includes sales, product, and customer data.
- **Dataset Availability**: Yes, the dataset is publicly available and can be found in this repository.

---

## **Technologies Used**

- **Power BI**: Utilized to create interactive dashboards and visualizations.
- **DAX**: Used for creating measures and calculated columns, including KPIs like total revenue, average order value, and repeat purchase rate.

### **Techniques Used**
- **Data Cleaning**: Ensured consistency in date, currency, and region-related columns.
- **DAX Functions**: Created several DAX measures for key metrics such as total revenue, repeat purchase rate, and customer lifetime value.
- **Conditional Formatting**: Applied to visuals for better clarity (e.g., color bars for performance metrics).

---

## **Data Modeling**
![image](https://github.com/user-attachments/assets/7ce3261f-25b9-42cc-9f82-e3b2263f2600)

### **Star Schema**
The data model follows a **star schema** design, consisting of two fact tables and several dimension tables to provide detailed insights.

- **Fact Tables**:
  - **Transactional Data**: Captures all sales-related data, including quantities sold, revenue, and cost associated with each transaction.
  - **Return Data**: Captures product returns, helping to assess return rates and their impact on the business.

- **Dimension Tables**:
  - **Customers**: Includes customer details such as ID, names, demographics (age, gender, occupation), and location (e.g., city, country).
  - **Products**: Contains product details like ID, name, category, and retail price.
  - **Regions**: Provides geographic data (country, state, city) to analyze performance by location.
  - **Stores**: Represents stores where products were sold, including store IDs and locations.
  - **Calendar**: Time-related data such as date, month, quarter, and year for time-based analysis.

### **Relationships**

- **Fact Tables** (Transactional Data and Return Data) are linked to dimension tables (Customers, Products, Regions, Stores, Calendar) via foreign keys.
- **Products** is connected through **Product ID**, **Customers** through **Customer ID**, and **Regions** via **Region ID**.
- **Stores** is linked to **Transactional Data** by **Store ID**, and **Calendar** connects to both fact tables via **Date**.
- **Regions** and **Stores** are connected, forming a **snowflake schema** relationship.

This hybrid schema (star and snowflake) enables efficient querying while ensuring better organization and reduced redundancy.

---

## **Visualizations**

The dashboard includes the following visualizations for data presentation:

- **KPIs**  
- **Matrix**  
- **Treemap**  
- **Gauge Chart**  
- **Bar Charts**  
- **Cards**  
- **Line Charts**  
- **Line and Column Chart**  
- **Slicers**  
- **Donut Charts**  
- **Maps**

---

## **Dashboard Pages**

### **1. Top-Line Performance Page**

On this page, key performance metrics like transaction values, profits, and return rates across product brands are explored. The main features include:

- **Matrix Visualization**: Displays total transactions, total profit, profit margin, and return rate by product brand.
- **Drillthrough Functionality**: Allows focusing on specific product brands by drilling through to the Product Brand Details page.
- **KPIs**: Displays KPIs for monthly revenue, current month transactions, current month profit, and returns.
- **Map**: Visualizes sales data by country, with drillthrough functionality for states and cities.
- **Treemap**: A hierarchical map showing data by country, state, and city.
- **Clustered Column Chart**: Weekly revenue trends.
- **Gauge Chart**: Compares actual revenue against target revenue.
- **Date Slicer**: A slider to filter data between the years 1997 and 1998 for time-based analysis.

![image](https://github.com/user-attachments/assets/d2fcbf65-d9a7-4681-a202-4785d0ae8d55)

### **2. Product Brand Details Page**

Provides in-depth details about selected product brands:
- **Brand Name Card**: Displays the selected brand, drilled through from the Top-Line Performance page.
- **Stacked Bar Chart**: Shows products sorted by revenue for the selected brand.
- **Pie Chart**: Displays revenue by price tier for the selected brand.
- **Donut Charts**: Visualizes the proportion of products that are low-fat and recyclable.
- **Gauge Chart**: Displays current month returns versus target returns for the selected brand.
- **Line Chart**: Weekly profit trends for the selected brand.
- **Area Chart**: Visualizes weekly returns trends.

![image](https://github.com/user-attachments/assets/c4421388-692a-4dd6-9faa-94d9830e9e9a)

### **3. Customer Details Page**

Focuses on customer-level analysis:
- **Table**: Displays customer names with total revenue and transactions.
- **KPI**: Shows monthly average basket size for customers.
- **Donut Charts**: Visualizes transaction distribution by gender and occupation.
- **Area Map**: Displays customer location data with drillthrough functionality.
- **Treemap**: Shows total transactions by age group.
- **Line Clustered Column Chart**: Monthly trends for transactions and revenue.
- **Cards**: Displays top customer by revenue and the customer with most orders.

![image](https://github.com/user-attachments/assets/1dbed253-b94f-447a-a323-7ea0712a8a53)

---

## **Data Cleaning & Transformation**

Key data cleaning and transformation steps included:

- **Standardized Data Formats**: Ensured consistency across date, currency, and region columns.
- **Created New Columns**: 
  - **Customer Table**: Created full name, year of birth, and customer behavior columns (e.g., "Has Children").
  - **Product Table**: Added discounted price and ensured proper encoding for categorical data.
  - **Store Table**: Created full address and extracted area code.
  - **Calendar Table**: Added time-related columns like the start of the week, day name, month name, quarter, and year.
- **Key Measures**:
  - **Revenue Measures**: Total Revenue, Monthly Revenue, Discounted Revenue, etc.  
  - **Profit Measures**: Total Profit, Profit Margin.  
  - **Customer Metrics**: Average Order Value (AOV), Repeat Purchase Rate, Customer Lifetime Value (CLV).  
  - **Transaction Metrics**: Total Transactions, Average Basket Size.  
  - **Return Metrics**: Return Rate, Total Returns.  

---

## **Challenges Faced**

- **Data Cleaning**: Handling missing data and formatting inconsistencies was challenging.
- **Handling Relationships**: Ensuring proper relationships between tables was crucial for the model’s functionality.

---

## **Key Takeaways**

- Product performance varies across brands and regions, with some areas significantly outperforming others.
- Data cleaning and transformation are critical before analysis.
- Drillthrough functionality enhanced the dashboard's interactivity.

---

## **Next Steps**

- **Expand Analysis**: Future analyses could include more years to identify longer-term trends.
- **Customer Segmentation**: More granular customer segmentation for deeper insights into specific purchasing behaviors.

---

## **Conclusion**

This dashboard serves as an effective tool for analyzing Maven Market's top-line performance, understanding customer behavior, and evaluating product performance across different time periods. The analysis provides valuable insights for informing strategic business decisions.

---
