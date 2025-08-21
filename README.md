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

1. Users & Events

   * 50 users (user_id 1001–1050) with 3–10 events each to simulate different engagement levels.

2. Sessions

   * Randomly assigned 1–5 sessions per user using the pattern: S<user_id><random_number>.

   * Supports session-based analysis.

3. Event Types

   * Randomly assigned: "view", "add_to_cart", "checkout", "purchase".

   * Models natural funnel drop-offs.

4. Products

   * product_id: random integer in a realistic range.

   * category: sampled from a predefined list.

   * price: uniformly random between $10–$500.

5. User Attributes

   * device and location sampled from predefined lists for segmentation.

6. Timestamps

  * Generated using Faker’s date_time_this_month() to simulate realistic user activity over one month.

7. Event IDs

  * Incremental unique ID for each row to maintain traceability.

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

