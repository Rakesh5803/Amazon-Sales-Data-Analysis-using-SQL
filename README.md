Here’s a clean, GitHub-ready report + SQL queries for your project 👇

📊 Amazon Sales Data Analysis using SQL
1. Project Title (Description) 📌
Amazon Sales Data Analysis using SQL Queries
This project focuses on analyzing e-commerce product and review data from
Amazon to extract meaningful insights such as pricing trends, discounts,
customer feedback, and product performance.

2. Problem ❗
Amazon has a large dataset of products and customer reviews. The challenge is
to:
 Identify valuable products based on pricing and ratings
 Analyze discount strategies
 Understand customer sentiment from reviews

3. Objective 🎯
 Analyze product pricing and discounts
 Filter products based on conditions
 Extract insights from customer reviews
 Practice real-world SQL queries

4. Dataset Overview 📂
The dataset includes:
 Product Name

 Category
 Actual Price
 Discounted Price
 Discount Percentage
 Rating
 Review Content

5. Tools and Techniques 🛠️
 SQL (MySQL / PostgreSQL)
 Data Filtering (WHERE)
 Pattern Matching (LIKE)
 Aggregation (AVG)
 String Functions

6. Formula Used 🧮
 Discount % Calculation (if needed):
SQL((actual_price - discounted_price) / actual_price) *100
 Average Difference:
SQLAVG(actual_price) - AVG(discounted_price)

7. Method (Steps) ⚙️
1. Load dataset into SQL database
2. Clean column names (if required)
3. Run queries based on conditions
4. Analyze output

5. Document insights

💻 SQL Queries
1. Products with discounted price < ₹500
SQLSELECT*
FROM products
WHERE discounted_price <500;

2. Products with discount 50% ≥
SQLSELECT*
FROM products
WHERE discount_percentage >=50;

3. Products containing "Cable"
SQLSELECT*
FROM products
WHERE product_name LIKE'%Cable%';

4. Difference between avg actual and discounted price per product
SQLSELECT product_name,
AVG(actual_price) - AVG(discounted_price) AS price_difference
FROM products
GROUPBY product_name;

5. Reviews mentioning "fast charging"
SQLSELECT*
FROM reviews
WHERE review_content LIKE'%fast charging%';

6. Discount between 20% and 40%
SQLSELECT*
FROM products
WHERE discount_percentage BETWEEN20AND40;

7. Products with price > ₹1000 and rating 4 ≥
SQLSELECT*
FROM products
WHERE actual_price >1000
AND rating >=4;

8. Discounted price ending with 9
SQLSELECT*
FROM products
WHERE discounted_price LIKE'%9';

9. Negative reviews (worst, waste, poor, not good)
SQLSELECT*
FROM reviews
WHERE review_content LIKE'%worst%'
OR review_content LIKE'%waste%'
OR review_content LIKE'%poor%'
OR review_content LIKE'%not good%';

10. Products in "Accessories" category
SQLSELECT*
FROM products
WHERE category LIKE'%Accessories%';

📈 8. Key Findings
 Many products offer heavy discounts (50%+)

 Lower-priced products (<₹500) dominate certain categories
 Keywords like “fast charging” appear frequently in tech reviews
 Negative reviews highlight quality issues

9. What We Accomplished ✅
 Built real-world SQL queries
 Extracted insights from raw data
 Identified customer sentiment
 Improved data analysis skills

10. Limitations ⚠️
 Dataset may not be fully clean
 Missing values can affect results
 Limited attributes (no time-based trends)

11. Future Opportunities 🚀
 Use Power BI for visualization
 Build dashboards
 Apply Machine Learning for sentiment analysis
 Predict product success

12. Recommendations 💡
 Improve product quality based on negative reviews
 Focus on high-rating, high-price products
 Optimize discount strategies

 Highlight fast-charging features in marketing

13. Conclusion 🏁
This project demonstrates how SQL can be used to analyze e-commerce data
effectively. It helps businesses make data-driven decisions related to pricing,
marketing, and customer satisfaction.
