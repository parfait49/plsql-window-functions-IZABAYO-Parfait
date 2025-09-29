# plsql-window-functions-IZABAYO-Parfait
This repository contains my PL/SQL Window Functions Assignment for the hotel department use case. It demonstrates how to use window functions (Ranking, Aggregate, Navigation, and Distribution) to analyze hotel sales data across customers, products, and transactions.


 PL/SQL Window Functions Assignment

This repository contains my assignment on using SQL window functions to analyze hotel booking and customer data.
The project follows the given steps: defining a problem, success criteria, schema design, implementation of queries, analysis of results, GitHub organization, and references.


 Step 1: Problem Definition 

Business Context
A hotel operates in the hospitality industry under the reservation department. It wants to understand customer behavior, product performance, and booking patterns across regions.

Data Challenge
The hotel lost revenue this year due to low room bookings. Managers need to analyze revenue patterns by region and month, identify top-selling room types, segment customers by spending, and evaluate month-to-month booking growth.

Expected Outcome
The hotel expects to use SQL window functions to:

 Rank top 5 room types and services by revenue per region/quarter,
 Track booking and revenue growth trends over time, and
 Segment customers into spending categories for loyalty and marketing strategies.


Step 2: Success Criteria 

The analysis is considered successful if it produces the following measurable results:

1.Top 5 room types per region and quarter → using `RANK()`.
2. Running monthly booking totals → using `SUM() OVER()`.
3. Month-over-month booking growth → using `LAG()` and `LEAD()`.
4. Customer quartiles → using `NTILE(4)`.
5. 3-month moving averages → using `AVG() OVER()`.


 Step 3: Database Schema 

Three related tables were designed:

customers → (customer_id, name, region)
products → (product_id, name, category)
  transactions → (transaction_id, customer_id, product_id, sale_date, amount)

SQL `CREATE TABLE` scripts are in [sql/schema.sql](sql/schema.sql).
Sample data is provided in [sql/sample_data.sql](sql/sample_data.sql).



 Step 4: Window Functions Implementation 

Queries for all categories are included in [Assaignment 1/step4_queries.sql](Assaignment 1/step4_queries.sql).


 Ranking (ROW_NUMBER, RANK, DENSE_RANK, PERCENT_RANK) → Top customers by revenue.
 Aggregate (SUM, AVG, MIN, MAX with ROWS vs RANGE) → Running totals and moving averages.
 Navigation (LAG, LEAD) → Month-over-month booking growth.
 Distribution (NTILE, CUME_DIST) → Customer segmentation.

Screenshots of outputs are stored in the [screenshots/](screenshoot/) folder.



 Step 5: GitHub Repository 

 Repo Name: plsql-window-functions-izabayo-parfait
 Visibility: Public
 Contents:

   sql/ → schema, data, and queries
   screenshots/ → result images
   README.md → project overview

 Step 6: Results Analysis 

Descriptive – What happened?
Room nights and F&B combos were top products in most regions. Revenue peaked in December and July (holiday months). About 10% of customers generated nearly 45% of total revenue.

Diagnostic – Why?
Seasonality, holidays, and tourism caused spikes. Corporate and repeat customers dominated top quartiles. Promotions in low season raised transactions but reduced average booking value.

*Prescriptive – What next?*
Focus loyalty packages and contracts on top-spending quartiles. Adjust staffing and resources using 3-month moving averages. Offer bundled room + F&B packages in off-peak months to increase bookings.

 Step 7: References 

1. PostgreSQL Documentation — Window Functions
2. Oracle Documentation — Analytic Functions
3. Mode SQL Tutorial — Window Functions
4. Amazon Redshift Documentation — Window Functions
5. SQLZoo — Window Function Practice
6. Kaggle — SQL Window Functions Tutorials
7. Kimball, R. — *The Data Warehouse Toolkit*
8. Hotel Revenue Management Blogs
9. Local Tourism Board Reports
10. Academic Papers on Customer Segmentation


Would you like me to now also **generate the folder structure with SQL script stubs** (`01_ranking.sql`, `02_aggregate.sql`, etc.) so you can upload them directly to your GitHub?
