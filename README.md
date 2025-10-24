# 🎯 Target — E-commerce Operations Analysis (Brazil)

![SQL](https://img.shields.io/badge/SQL-Google%20BigQuery-blue.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![Dataset](https://img.shields.io/badge/Dataset-Target_Brazil-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 📘 About Target

**Target** is a globally renowned retail brand headquartered in the United States.  
It has established itself as a **preferred shopping destination** by offering:
- Outstanding value 💰  
- Inspiring innovation 💡  
- Exceptional guest experiences 🌟  

---

## 🌎 Project Context

This business case focuses on **Target’s operations in Brazil**, analyzing **100,000 customer orders** placed between **2016 and 2018**.  

The dataset provides a comprehensive view of:
- Order status and fulfillment  
- Product pricing and payment behavior  
- Freight and shipping performance  
- Customer demographics and locations  
- Product characteristics and customer reviews  

Through this data, we uncover insights into:
- Operational efficiency ⚙️  
- Pricing and delivery strategies 🚚  
- Customer satisfaction trends 💬  
- Market demand patterns 📊  

---

## 🔍 Analysis Platform

**Analyzed Using:**  
💻 **Google BigQuery** (SQL-based data exploration and analytics)

---

## 📚 Dataset Overview

The dataset is provided in **8 CSV files**, each representing a key dimension of Target’s operations:

| File Name | Description |
|------------|--------------|
| `customers.csv` | Customer demographic information |
| `geolocation.csv` | Location details (latitude, longitude, and postal codes) |
| `order_items.csv` | Product-level details per order |
| `payments.csv` | Payment type and transaction values |
| `reviews.csv` | Customer feedback and review scores |
| `orders.csv` | Order lifecycle and timestamps |
| `products.csv` | Product details and specifications |
| `sellers.csv` | Seller information and location |

---

## 🧾 Feature Descriptions

### 👥 **customers.csv**
| Feature | Description |
|----------|-------------|
| customer_id | Unique ID of the customer |
| customer_unique_id | Permanent unique ID of the customer |
| customer_zip_code_prefix | Zip code prefix of customer’s location |
| customer_city | City name of the customer |
| customer_state | State code (e.g., São Paulo – SP) |

---

### 🏪 **sellers.csv**
| Feature | Description |
|----------|-------------|
| seller_id | Unique ID of the seller |
| seller_zip_code_prefix | Seller’s zip code prefix |
| seller_city | Seller’s city |
| seller_state | Seller’s state code |

---

### 📦 **order_items.csv**
| Feature | Description |
|----------|-------------|
| order_id | Unique ID of the customer order |
| order_item_id | Unique ID for each item within the order |
| product_id | Unique ID for each product |
| seller_id | Seller’s unique identifier |
| shipping_limit_date | Date before which the order must be shipped |
| price | Price of the product |
| freight_value | Freight (shipping) cost |

---

### 🌍 **geolocation.csv**
| Feature | Description |
|----------|-------------|
| geolocation_zip_code_prefix | First 5 digits of the postal code |
| geolocation_lat | Latitude coordinate |
| geolocation_lng | Longitude coordinate |
| geolocation_city | City name |
| geolocation_state | State name |

---

### 💳 **payments.csv**
| Feature | Description |
|----------|-------------|
| order_id | Unique ID of the order |
| payment_sequential | Payment sequence number (for EMIs) |
| payment_type | Mode of payment (e.g., Credit Card) |
| payment_installments | Number of installments (if EMI) |
| payment_value | Total amount paid |

---

### 📅 **orders.csv**
| Feature | Description |
|----------|-------------|
| order_id | Unique ID of the order |
| customer_id | Customer’s unique identifier |
| order_purchase_timestamp | Order purchase date and time |
| order_delivered_carrier_date | Date when carrier received the order |
| order_delivered_customer_date | Date when customer received the order |
| order_estimated_delivery_date | Expected delivery date |

---

### 💬 **reviews.csv**
| Feature | Description |
|----------|-------------|
| review_id | Unique ID of each review |
| order_id | Associated order ID |
| review_score | Rating (1–5) given by customer |
| review_comment_title | Review title |
| review_comment_message | Review text |
| review_creation_date | Date when review was created |
| review_answer_timestamp | Timestamp when review was answered |

---

### 🛍️ **products.csv**
| Feature | Description |
|----------|-------------|
| product_id | Unique product identifier |
| product_category_name | Category of the product |
| product_name_lenght | Length of the product name string |
| product_description_lenght | Length of the product description |
| product_photos_qty | Number of product photos |
| product_weight_g | Product weight (grams) |
| product_length_cm | Product length (cm) |
| product_height_cm | Product height (cm) |
| product_width_cm | Product width (cm) |

---

## 🧩 Dataset Schema

![Dataset Schema](https://github.com/ankit-verma2000/Target-sql-/assets/150786247/e71ca94d-0350-47be-acbd-619108ca5ecd)

---

## 📈 Data Interpretation & Insights

### 📊 Exploratory Analysis (2016–2018)
Conducted exploratory analysis on **100,000 customer orders** across Brazil using **SQL in Google BigQuery**.

---

### 🔑 **Key Metrics**
- Analyzed **city and state-level distributions** of orders.
- Identified **seasonal purchase trends** across multiple years.

---

### 📅 **Seasonal Trends**
- E-commerce orders showed **steady growth** over time.  
- **January**: +70% increase in order value  
- **February**: +20% increase  
- **April**: +10% increase  
➡️ Indicates high seasonal demand at the start of the year.

---

### 👥 **Customer Behavior**
- Peak shopping times: **Afternoons** and **Nights**  
- Indicates potential for **targeted marketing** during these hours.

---

### 💰 **Order Value Analysis**
- Calculated **total and average order value** by state.  
- **São Paulo (SP)** had the **highest total sales value**,  
  but **lowest average order price**, suggesting a **large volume of lower-value purchases**.

---

### 🚚 **Delivery Insights**
- Evaluated delivery efficiency by state:
  - **São Paulo (SP)** → Fastest average delivery times  
  - **Roraima (RR)** → Longest delivery delays  
- Some states experienced deliveries **up to 20 days earlier** than estimated.

---

### 💳 **Payment Methods**
- **Credit Card** emerged as the **most preferred payment method**, followed by **Boleto (invoice)**.

---

### 🚀 **Actionable Insights**
✅ Optimize **delivery operations** in high-delay regions.  
✅ Focus **marketing campaigns** during high-traffic time slots (afternoons & nights).  
✅ Enhance **customer retention** via improved delivery tracking and satisfaction programs.  
✅ Promote **installment-based payment offers** to drive conversions.

---

## 🛠️ Tech Stack

| Tool / Technology | Purpose |
|--------------------|----------|
| **Google BigQuery (SQL)** | Data querying & analysis |
| **Google Cloud Platform (GCP)** | Cloud data storage |
| **Excel / Sheets** | Supporting analysis and validation |
| **Data Visualization Tools** | Charts, KPIs, and dashboards for insights |

---

## 👨‍💻 Author  
**Ankit Verma**  
_Data Analyst | SQL • Python • Power BI • Data Visualization_  
🔗 [LinkedIn](https://www.linkedin.com/in/ankitvermads/) • [GitHub](https://github.com/ankit-verma2000)

---

⭐ **If you found this project insightful, consider giving it a star on GitHub!** ⭐
