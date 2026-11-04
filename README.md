#### 🛒 Ecommerce Sales Dashboard

An interactive and dynamic **Ecommerce Sales Dashboard** designed to track, analyze, and visualize key sales performance metrics. This project helps businesses extract actionable insights regarding sales revenue, profitability, customer behavior, and regional trends. 

#### 📊 Project Overview & Key Insights

This dashboard provides a comprehensive breakdown of e-commerce performance: 

* **Key Performance Indicators (KPIs):** Tracks Total Quantity (2K), Sum of Amount (161K), Sum of Profit (26K), and Sum of AOV (44K).
* **Geographical Performance:** Top-performing states filtered by total sales amount (Maharashtra, Madhya Pradesh, Delhi, Uttar Pradesh).
* **Category Breakdown:** Share of total quantity sold divided into Clothing (63%), Electronics (19%), and Furniture (18%).
* **Monthly Trends:** Profit analysis across consecutive months (January, February, March).
* **Customer Preferences:** Analysis of top-buying customers and preferred payment methods (COD, UPI, Debit Card, Credit Card).

#### 🛠️ Tech Stack & Tools Used

* **BI Tool:** Microsoft Power BI Desktop
* **Data Source:** E-commerce Sales Dataset (CSV/Excel format)
* **Data Transformation:** Power Query Editor
* **Modeling:** DAX (Data Analysis Expressions)

#### 💻 Technical Implementation & DAX Code

To create dynamic KPIs and calculated columns, the following **DAX (Data Analysis Expressions)** formulas were implemented in this project: 

#### 1. Total Sales Amount

dax

Total_Sales_Amount = SUM(Sales_Data[Amount])

#### 2. Total Profit Calculated

dax

Total_Profit = SUM(Sales_Data[Profit])


#### 3. Average Order Value (AOV)

dax

Average_Order_Value = DIVIDE([Total_Sales_Amount], SUM(Sales_Data[Quantity]), 0)

#### 4. Dynamic Quarter Category (Power Query / M-Code representation)

powerquery

= Table.AddColumn(#"Changed Type", "Quarter", each if [Month] = "January" or [Month] = "February" or [Month] = "March" then "Qtr 1" else "Other")


 
