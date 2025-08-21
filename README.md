# 📊 E-commerce-Funnel-Analysis

#### 🤌 Business Problem
E-commerce businesses often lose users at different funnel stages:
Visit → Product View → Add to Cart → Checkout → Purchase

#### 📌 Objective 
Identify where users drop off and recommend strategies to increase conversions.

#### This data was simulated
1️⃣ Purpose
The dataset simulates user interactions on an e-commerce platform to analyze funnel conversion, user behavior, and product performance. It is designed for SQL analysis, dashboarding, and data visualization.

2️⃣ Dataset Schema

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

3️⃣ Data Generation Methodology

Users and Events

50 users (user_id 1001–1050) are simulated.

Each user has 3–10 events generated randomly to mimic variable engagement.

Sessions

Session IDs combine user ID + random number (1–5 sessions per user).

Allows session-based analytics (e.g., session conversion rate).

Event Types

Randomly selected from ["view", "add_to_cart", "checkout", "purchase"].

Simulates natural funnel drop-offs — not all users complete every stage.

Products

product_id: random integer in a realistic range.

category: sampled from a predefined list.

price: continuous uniform distribution between 10–500 USD.

User Attributes

device and location sampled from predefined lists to allow segmentation.

Timestamps

Generated using Faker’s date_time_this_month() to simulate events within a single month.

Enables time-based analysis and trend tracking.

4️⃣ Implementation Notes

* Language: Python 3.x

* Libraries: pandas, faker, random

* Output: CSV file or Pandas DataFrame, easily loaded into SQL or BI tools.

* Randomness: Can set a seed for reproducibility.

5️⃣ Use Cases

* Funnel conversion analysis (view → add → checkout → purchase).

* Time-to-purchase analysis by product, category, device, or location.

* Segmentation analysis for marketing or UX improvements.

* Feeding into dashboards in Streamlit, Tableau, or Looker Studio.

