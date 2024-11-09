# Source Data
This folder contains the source CSV files used to populate the data warehouse. Each file represents a distinct entity or aspect of the e-commerce dataset. Below is a summary of each file's contents, along with the columns in each file.

## File Descriptions
•  **order.csv:**
Contains details for each customer order, including order status and key dates.

Columns: order_id, user_name, order_status, order_date, order_approved_date, pickup_date, delivered_date, estimated_time_deliveryd

•  **feedback.csv:**
Stores customer feedback related to orders, with fields for feedback score and timestamps for form submission and response.

Columns: feedback_id, order_id, feedback_score, feedback_form_sent_date, feedback_answer_date

•  **order_item.csv:**
Lists individual items within each order, capturing details like product ID, seller ID, price, shipping cost, and the pickup deadline.

Columns: order_id, order_item_id, product_id, seller_id, pickup_limit_date, price, shipping_cost

•  **payment.csv:**
Holds payment information for each order, including payment type, installments, and total payment value.

Columns: order_id, payment_sequential, payment_type, payment_installments, payment_value

•  **product.csv:**
Contains product details, such as category, name length, description length, weight, and dimensions.

Columns: product_id, product_category, product_name_lenght, product_description_lenght, product_photos_qty, product_weight_g, product_length_cm, product_height_cm, product_width_cm

•  **sellers.csv:**
Provides information about each seller, including location details.

Columns: seller_id, seller_zip_code, seller_city, seller_state

•  **users.csv:**
Contains user information, supporting demographic and regional analysis.

Columns: user_name, customer_zip_code, customer_city, customer_state
