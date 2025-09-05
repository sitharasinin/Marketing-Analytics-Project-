# American Express - Customer Offer Analysis

## Project Objective
This project analyzes a large, anonymized clickstream dataset to uncover insights into customer behavior in response to American Express's marketing offers. The goal was to solve key business questions regarding user activity, offer performance, and customer spending habits while navigating data ambiguity.

## Tools Used
* **Python:** Pandas for data manipulation and analysis.
* **SQL (via SQLite):** For efficient data aggregation, transformation, and complex queries, including the use of window functions.
* **Tableau:** For creating a final summary dashboard of key findings.

## Analytical Approach
The raw data was anonymized, requiring a hypothesis-driven approach:
1.  **Data Exploration:** Identified data types, distributions, and missing values.
2.  **Hypothesis Formation:** Used methods like analyzing unique value counts (`.nunique()`) and statistical summaries (`.describe()`) to form logical hypotheses for critical columns like `offer_category`, `spend_amount`, and `discount_value`.
3.  **Data Transformation:** Built a final, enriched table (`clickstream_final`) with a new `is_active_user` flag, calculated using SQL window functions.
4.  **Segmentation & Analysis:** Divided customers into three equal spending tiers (Low, Medium, High) to perform a comparative analysis on offer engagement.

## Key Findings
* **Finding 1 (Q1):** While active users who clicked on offers tended to save more money, it was the **inactive users** who surprisingly showed a higher click-through rate across all offer categories.
* **Finding 2 (Q2):** Across all identified offer types, customers consistently responded better to offers with a **'High Discount Value per Dollar'**.
* **Finding 3 (Q3):** The **MEDIUM** spending segment was the best-performing, showing the highest engagement compared to Low and High spenders.
* **Finding 4 (Q4):** A profile of the top 10 highest-converting offers was built, providing a list of the most effective offers that were shown to a significant number of users.

## Interactive Dashboard
An interactive summary of these findings can be viewed on Tableau Public:

 https://public.tableau.com/app/profile/sithara.sinin/viz/CustomerBehaviorAnalysisforFinancialServicesOffers/CustomerBehaviorAnalysisforFinancialServicesOffers 
