# 📊 E-commerce-Funnel-Analysis

## Business Problem
E-commerce businesses often lose users at different funnel stages:
Visit → Product View → Add to Cart → Checkout → Purchase

## Objective 
Identify where users drop off and recommend strategies to increase conversions.

# 📂 Dataset Schema: ecommerce_events

| Column Name  | Type      | Description                                                         |
| ------------ | --------- | ------------------------------------------------------------------- |
| `event_id`   | INTEGER   | Unique ID for each event                                            |
| `user_id`    | INTEGER   | Unique customer identifier                                          |
| `session_id` | STRING    | Session identifier (to group user actions)                          |
| `event_time` | TIMESTAMP | Date & time of event                                                |
| `event_type` | STRING    | Funnel stage: `"view"`, `"add_to_cart"`, `"checkout"`, `"purchase"` |
| `product_id` | INTEGER   | Unique product identifier                                           |
| `category`   | STRING    | Product category (e.g., Electronics, Clothing, Home)                |
| `price`      | FLOAT     | Price of the product                                                |
| `device`     | STRING    | `"mobile"`, `"desktop"`, `"tablet"`                                 |
| `location`   | STRING    | User location (city/country)                                        |

