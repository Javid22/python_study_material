This is where you can turn your project into something that looks like a **real client engagement** rather than just a collection of charts.
Since you're using the **Olist Brazilian E-Commerce Dataset**, imagine you're working as a **Data Analyst** for the company's leadership team.
---
# Project Title
**E-Commerce Sales Performance & Customer Insights Dashboard**
---
# Business Scenario
> Olist is an e-commerce marketplace connecting customers and sellers across Brazil. Management wants to understand sales performance, customer behavior, delivery efficiency, seller performance, and product trends to improve profitability and customer satisfaction.
Your job is to analyze the data and present actionable business recommendations.
---
# Project Objectives
Your goals are to:
* Assess data quality.
* Clean and prepare the data.
* Merge multiple datasets into a single analytical dataset.
* Explore business performance through EDA.
* Build meaningful visualizations.
* Recommend actions based on insights.
---
# Phase 1: Data Understanding
Before writing any code, answer:
* How many datasets are there?
* What does each dataset represent?
* What is the primary key of each table?
* How are the datasets related?
* Why is normalization used instead of one large table?
Explain this as if you're introducing the database to a client.
---
# Phase 2: Data Cleaning
Document every step.
## Questions
### Missing Values
* Which columns contain missing values?
* What percentage is missing?
* Can the missing data be ignored?
* Should it be removed or filled?
---
### Duplicate Records
* Are there duplicate orders?
* Duplicate customers?
* Duplicate sellers?
* Duplicate reviews?
---
### Data Types
* Are dates stored correctly?
* Are IDs stored as strings?
* Are numeric columns the correct type?
---
### Invalid Data
* Negative prices?
* Zero freight value?
* Future timestamps?
* Invalid ZIP codes?
---
### Outliers
* Products with unusually high prices?
* Extremely expensive freight?
* Sellers with exceptionally high sales?
Explain how you identified and handled outliers.
---
# Phase 3: Exploratory Data Analysis (EDA)
## Sales
Questions:
* Total revenue?
* Total number of orders?
* Average order value?
* Monthly sales trend?
* Yearly sales trend?
* Best month?
* Worst month?
Visuals:
* KPI cards
* Line chart
* Monthly trend
---
## Customers
Questions:
* Number of customers?
* Which states have the most customers?
* Which cities generate the highest revenue?
* New vs returning customers (if identifiable)
Visuals:
* Bar chart
* Map (if available)
---
## Products
Questions:
* Best-selling categories?
* Lowest-selling categories?
* Average product price?
* Categories with the highest freight cost?
Visuals:
* Horizontal bar chart
* Treemap
* Box plot
---
## Sellers
Questions:
* Top sellers by revenue?
* Top sellers by number of orders?
* Seller distribution by state?
* Which sellers receive better ratings?
Visuals:
* Bar chart
* Bubble chart
---
## Reviews
Questions:
* Average review score?
* Rating distribution?
* Which categories receive poor reviews?
* Does delivery time affect ratings?
Visuals:
* Histogram
* Bar chart
* Scatter plot
---
## Delivery
Questions:
* Average delivery time?
* Fastest deliveries?
* Delayed deliveries?
* Delivery performance by state?
* Delivery performance by seller?
Visuals:
* Histogram
* Box plot
* Line chart
---
## Payments
Questions:
* Most used payment method?
* Average installment count?
* Revenue by payment type?
Visuals:
* Pie chart
* Donut chart
---
# Phase 4: Feature Engineering
Create meaningful derived columns, such as:
* Order Month
* Order Year
* Delivery Days
* Shipping Delay
* Weekend Order
* Quarter
* Revenue Category
* Freight Percentage
Explain why each new feature is useful.
---
# Phase 5: Business Questions
These are the kinds of questions stakeholders care about:
### Sales
* Which product categories should receive more investment?
* Which categories are underperforming?
### Customers
* Which regions are our strongest markets?
* Which regions need marketing attention?
### Sellers
* Which sellers contribute the most revenue?
* Which sellers have slow deliveries?
### Logistics
* Does longer delivery time reduce customer ratings?
* Which states have the slowest deliveries?
### Product Strategy
* Which categories have high sales but low ratings?
* Which categories have low sales but high ratings?
### Payments
* Which payment method is most popular?
* Does installment usage affect order value?
---
# Phase 6: Dashboard
Your dashboard should include:
### KPI Cards
* Total Revenue
* Total Orders
* Total Customers
* Average Order Value
* Average Review Score
* Average Delivery Time
* Number of Sellers
* Number of Products
### Visualizations
* Monthly Sales Trend
* Revenue by Category
* Top Sellers
* Top States
* Delivery Time Distribution
* Payment Method Distribution
* Review Score Distribution
* Sales by State (Map)
* Category Performance
* Freight Cost Analysis
---
# Phase 7: Insights
Avoid saying:
> "This chart shows..."
Instead, focus on business meaning.
For example:
* Technology products contribute the highest revenue.
* Most customers are concentrated in a few key states.
* Delivery delays are associated with lower review scores.
* A small number of sellers account for a large share of revenue.
---
# Phase 8: Recommendations
Translate insights into actions.
Examples:
* Expand inventory for high-performing categories.
* Improve logistics in regions with long delivery times.
* Support lower-performing sellers with training.
* Reduce freight costs for expensive categories.
* Investigate categories with high sales but poor customer ratings.
---
# Phase 9: Limitations
A professional presentation also acknowledges what's missing.
For example:
* Profit information isn't available, so the analysis focuses on revenue.
* Marketing campaign data isn't included.
* Customer demographics are limited.
* Inventory levels are unavailable.
---
# Phase 10: Future Scope
Suggest how the analysis could be extended:
* Sales forecasting
* Customer segmentation (RFM analysis)
* Customer lifetime value
* Recommendation systems
* Demand forecasting
* Churn prediction
* Sentiment analysis on review text
---
## How to present this to a client
Structure your presentation like this:
1. Business Problem
2. Dataset Overview
3. Data Cleaning Process
4. Data Model (how the tables relate)
5. Exploratory Analysis
6. Dashboard Walkthrough
7. Key Insights
8. Business Recommendations
9. Limitations
10. Future Enhancements
This structure mirrors the flow many data analysts use in consulting projects and demonstrates not just technical skills, but also the ability to communicate findings in a way that supports business decisions.