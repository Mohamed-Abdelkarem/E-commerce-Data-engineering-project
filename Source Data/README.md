# Source Data

This folder contains the original CSV files used to populate the e-commerce data warehouse. Each file represents a distinct entity or aspect of the dataset, serving as the foundation for the fact and dimension tables in the warehouse. Below, each file is listed with a description and the columns it includes.

<img src="https://github.com/Mohamed-Abdelkarem/e-commerce-data-engineering-project-/blob/main/Source%20Data/source_data.png" alt="dimensional model" width="790" height="530">


## File Descriptions

### `order.csv`  
Contains details for each customer order, including order status and key dates.  
- **Columns**:  
  - `order_id`: Unique identifier for each order.  
  - `user_name`: The name of the user who placed the order.  
  - `order_status`: Current status of the order (e.g., approved, shipped, delivered).  
  - `order_date`: Date when the order was placed.  
  - `order_approved_date`: Date when the order was approved.  
  - `pickup_date`: Scheduled date for pickup.  
  - `delivered_date`: Date when the order was delivered.  
  - `estimated_time_delivery`: Estimated time for delivery completion.

---

### `feedback.csv`  
Stores customer feedback related to orders, including feedback scores and timestamps.  
- **Columns**:  
  - `feedback_id`: Unique identifier for each feedback entry.  
  - `order_id`: Identifier linking feedback to a specific order.  
  - `feedback_score`: Numerical score provided by the customer.  
  - `feedback_form_sent_date`: Date the feedback form was sent.  
  - `feedback_answer_date`: Date when the feedback was received.

---

### `order_item.csv`  
Lists individual items within each order, capturing item-specific details such as product ID, price, and shipping cost.  
- **Columns**:  
  - `order_id`: Identifier linking the item to a specific order.  
  - `order_item_id`: Unique identifier for each item within an order.  
  - `product_id`: Identifier for the product.  
  - `seller_id`: Identifier for the seller of the item.  
  - `pickup_limit_date`: Last date for scheduled pickup.  
  - `price`: Price of the item.  
  - `shipping_cost`: Cost of shipping for the item.

---

### `payment.csv`  
Contains payment transaction details for each order, including payment type and total amount.  
- **Columns**:  
  - `order_id`: Identifier linking the payment to a specific order.  
  - `payment_sequential`: Sequence number of the payment within the order.  
  - `payment_type`: Type of payment (e.g., credit card, debit card).  
  - `payment_installments`: Number of payment installments.  
  - `payment_value`: Total payment value.

---

### `product.csv`  
Includes product-specific information such as category, dimensions, and weight, useful for detailed product analysis.  
- **Columns**:  
  - `product_id`: Unique identifier for each product.  
  - `product_category`: Category to which the product belongs.  
  - `product_name_lenght`: Length of the product name.  
  - `product_description_lenght`: Length of the product description.  
  - `product_photos_qty`: Number of photos associated with the product.  
  - `product_weight_g`: Weight of the product in grams.  
  - `product_length_cm`: Length of the product in centimeters.  
  - `product_height_cm`: Height of the product in centimeters.  
  - `product_width_cm`: Width of the product in centimeters.

---

### `sellers.csv`  
Provides information about sellers, including location details.  
- **Columns**:  
  - `seller_id`: Unique identifier for each seller.  
  - `seller_zip_code`: Zip code of the seller’s location.  
  - `seller_city`: City where the seller is located.  
  - `seller_state`: State where the seller is located.

---

### `users.csv`  
Contains user demographic information, supporting analysis of customer behavior by region.  
- **Columns**:  
  - `user_name`: Unique identifier for each user.  
  - `customer_zip_code`: Zip code of the customer’s location.  
  - `customer_city`: City where the customer is located.  
  - `customer_state`: State where the customer is located.
