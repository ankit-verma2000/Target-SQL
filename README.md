# Target:

# Context:

- Target is a globally renowned brand and a prominent retailer in the United States. Target makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation, and an exceptional guest experience that no other retailer can deliver.

- This particular business case focuses on the operations of Target in Brazil and provides insightful information about 100,000 orders placed between 2016 and 2018. The dataset offers a comprehensive view of various dimensions including the order status, price, payment and freight performance, customer location, product attributes, and customer reviews.

- By analyzing this extensive dataset, it becomes possible to gain valuable insights into Target's operations in Brazil. The information can shed light on various aspects of the business, such as order processing, pricing strategies, payment and shipping efficiency, customer demographics, product characteristics, and customer satisfaction levels.

___________________________________________________________________________________________________________

🔎Analyze the dataset in <b><code>Google BigQuery </code></b>

📚 The dataset is available in 8 CSV files:

1. customers.csv 
2. geolocation.csv 
3. order_items.csv 
4. payments.csv 
5. reviews.csv 
6. orders.csv 
7. products.csv 
8. sellers.csv
   
<br/> <hr/>
The column description for these CSV files is given below.

The customers.csv contains the following features:

Features | Description | 
--- | --- 
customer_id | ID of the consumer who made the purchase | 
customer_unique_id | Unique ID of the consumer | 
customer_zip_code_prefix | Zip Code of consumer’s location | 
customer_city | Name of the City from where the order is made | 
customer_state | State Code from where the order is made (Eg. são Paulo - SP) |

<br/> <hr/>

The sellers.csv contains the following features:

Features | Description | 
--- | --- 
seller_id | Unique ID of the seller registered | 
seller_zip_code_prefix | Zip Code of the seller’s location | 
seller_city | Name of the City of the seller | 
seller_state | State Code (Eg. são paulo - SP) | 

<br/> <hr/>

The order_items.csv contains following features:

Features | Description | 
--- | --- 
order_id | A Unique ID of order made by the consumers | 
order_item_id | A Unique ID given to each item ordered in the order | 
product_id | A Unique ID given to each product available on the site | 
seller_id | Unique ID of the seller registered in Target | 
shipping_limit_date | The date before which the ordered product must be shipped | 
price | Actual price of the products ordered | 
freight_value | Price rate at which a product is delivered from one point to another | 

<br/> <hr/>

The geolocations.csv contains following features:

Features | Description | 
--- | --- 
geolocation_zip_code_prefix | First 5 digits of Zip Code | 
geolocation_lat | Latitude | 
geolocation_lng | Longitude | 
geolocation_city | City | 
geolocation_state | State | 

<br/> <hr/>

The payments.csv contains following features:

Features | Description | 
--- | --- 
order_id | A Unique ID of order made by the consumers | 
payment_sequential | Sequences of the payments made in case of EMI | 
payment_type | Mode of payment used (Eg. Credit Card) | 
payment_installments | Number of installments in case of EMI purchase | 
payment_value | Total amount paid for the purchase order | 


<br/> <hr/>

The orders.csv contains following features:

Features | Description | 
--- | --- 
order_id | A Unique ID of order made by the consumers | 
customer_id | ID of the consumer who made the purchase | 
order_purchase_timestamp | Status of the order made i.e. delivered, shipped, etc. | 
order_delivered_carrier_date | Delivery date at which carrier made the delivery | 
order_delivered_customer_date | Date at which customer got the product | 
order_estimated_delivery_date | Estimated delivery date of the products | 


<br/> <hr/>

The reviews.csv contains following features:

Features | Description | 
--- | --- 
review_id | ID of the review given on the product ordered by the order id | 
order_id | A Unique ID of order made by the consumers | 
review_score | Review score given by the customer for each order on a scale of 1-5 | 
review_comment_title | Title of the review | 
review_comment_message | Review comments posted by the consumer for each order | 
review_creation_date | Timestamp of the review when it is created | 
review_answer_timestamp | Timestamp of the review answered | 


<br/> <hr/>

The products.csv contains the following features:

Features | Description | 
--- | --- 
product_id | A Unique identifier for the proposed project. | 
product_category_name | Name of the product category | 
product_name_lenght | Length of the string which specifies the name given to the products ordered | 
product_description_lenght | Length of the description written for each product ordered on the site | 
product_photos_qty | Number of photos of each product ordered available on the shopping portal | 
product_weight_g | Weight of the products ordered in grams | 
product_length_cm | Length of the products ordered in centimeters | 
product_height_cm | Height of the products ordered in centimeters | 
product_width_cm | Width of the product ordered in centimeters | 

___________________________________________________________________________________________________________
**Dataset schema:**

![image](https://github.com/ankit-verma2000/Target-sql-/assets/150786247/e71ca94d-0350-47be-acbd-619108ca5ecd)

------------
# Interpretation:

**Conducted exploratory analysis on customer orders from 2016-2018 in Brazil.**

𝐊𝐞𝐲 𝐌𝐞𝐭𝐫𝐢𝐜𝐬: Analyzed city, state distributions, and periods of customer orders.

𝐒𝐞𝐚𝐬𝐨𝐧𝐚𝐥 𝐓𝐫𝐞𝐧𝐝𝐬: Identified a growing trend in e-commerce orders with fluctuations. Notably, January showed a 70% increase in order costs, followed by 20% in February and 10% in April.

𝐂𝐮𝐬𝐭𝐨𝐦𝐞𝐫 𝐁𝐞𝐡𝐚𝐯𝐢𝐨𝐫: Determined peak order times during afternoons and nights.

𝐎𝐫𝐝𝐞𝐫 𝐕𝐚𝐥𝐮𝐞 𝐀𝐧𝐚𝐥𝐲𝐬𝐢𝐬: Calculated total and average order prices and freight costs across states. São Paulo had the highest total order value but the lowest average price.

𝐃𝐞𝐥𝐢𝐯𝐞𝐫𝐲 𝐈𝐧𝐬𝐢𝐠𝐡𝐭𝐬: Assessed delivery times, highlighting São Paulo(SP) with the shortest average delivery time, while Roraima had the longest. The fastest deliveries occurred up to 20 days earlier than estimated in some states.

𝐏𝐚𝐲𝐦𝐞𝐧𝐭 𝐌𝐞𝐭𝐡𝐨𝐝𝐬:Evaluated payment types, revealing credit card as the most popular method.

𝐀𝐜𝐭𝐢𝐨𝐧𝐚𝐛𝐥𝐞 𝐈𝐧𝐬𝐢𝐠𝐡𝐭𝐬: Suggested improvements in delivery times, customer retention, and marketing strategies.

𝐓𝐞𝐜𝐡 𝐒𝐭𝐚𝐜𝐤: SQL (Data Analysis)
