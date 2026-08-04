Phase 1: Merging multiple data

Step 1 — Core 4-way INNER JOIN (on order_id):
  Files   : olist_orders_dataset.csv
            olist_order_items_dataset.csv
            olist_order_payments_dataset.csv
            olist_order_reviews_dataset.csv
  Purpose : Build the central fact table by linking every order with its
            purchased items, payment details, and customer review.
            Inner join ensures only orders with all four records are included.

Step 2 — Products LEFT JOIN (on product_id):
  File    : olist_products_dataset.csv
  Purpose : Attach product details (category name, dimensions, weight,  photo count) to each order item. Left join retains all orders even if product
            info is missing.

Step 3 — Sellers LEFT JOIN (on seller_id):
  File    : olist_sellers_dataset.csv
  Purpose : Add seller location info (city, state, ZIP prefix) to each order item
            to support seller-level and regional sales analysis.

Step 4 — Customers LEFT JOIN (on customer_id):
  File    : olist_customers_dataset.csv
  Purpose : Add customer location info (city, state, ZIP prefix) to support
            customer demographics and regional demand analysis.

Step 5 — Geolocation LEFT JOIN (on customer_zip_code_prefix):
  File    : olist_geolocation_dataset.csv
            (pre-aggregated to one record per ZIP prefix using mean lat/lng)
  Purpose : Attach latitude and longitude coordinates to each customer ZIP
            prefix for geospatial mapping and delivery distance analysis.
            Aggregation done first to prevent duplicate row explosion.


Phase 2: Data Cleaning

drop duplicate values after merging

order_approved_at: which 25 data are null whcih status as delivered
 i have drop those record it wont impact beacuse it has very minimun records

order_delivered_carrier_date:
canceled       483
invoiced       370
processing     370
unavailable      7
approved         3
delivered        2

After data validation, 3 delivered orders were identified with missing carrier and customer delivery dates. These records represent 0.003% of the dataset and have no material impact on overall business insights. They were retained in the master dataset for data integrity but excluded from delivery duration calculations where accurate timestamps were required

order_delivered_customer_date:
shipped        1167
canceled        546
invoiced        370
processing      370
delivered         8
unavailable       7
approved          3

After data validation, 3 delivered orders were identified with missing carrier and customer delivery dates. These records represent 0.008% of the dataset and have no material impact on overall business insights. They were retained in the master dataset for data integrity but excluded from delivery duration calculations where accurate timestamps were required

I have been updating no comments on empty review_comment_title and review_comment_message  

product_category_name :
i have cleched seller_id which not empty and check all seller are same using unique(). if yes i will replicated those product_category_name to specific seller_id

geolocation:
The geolocation dataset was aggregated to one record per ZIP code prefix before merging to avoid duplicate records. After the merge, 316 customer ZIP code prefixes (approximately 0.27% of the dataset) had no matching geolocation record. These transactions were retained because their business information remained valid, while they were excluded only from geospatial analyses requiring latitude and longitude

Phase 3: Exploratory Data Analysis (EDA)
