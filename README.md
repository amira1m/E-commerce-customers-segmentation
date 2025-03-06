Customer Segmentation Project 
Overview : 
This project applies unsupervised learning to segment customers based on their transactional behavior. By understanding customer interactions, businesses can design targeted marketing strategies to improve engagement and retention.

Approach : 
1. Data Processing
Loaded customer, transaction, and branch data from an Excel file.
Merged relevant tables to create a complete customer profile.
Converted date columns (transaction_date, burn_date) and calculated "time to burn" (number of days between transaction and coupon usage).
Handled missing values by filling with the column mean.
2. Feature Engineering
Aggregated transaction data at the customer level, extracting:
Number of transactions per customer.
Average time to burn a coupon.
Burn ratio (percentage of coupons used).
Encoded categorical variables (city_name, gender_name) using Label Encoding.
Standardized numerical features using StandardScaler for better clustering performance.
3. Clustering Model (K-Means)
Used the Elbow Method to determine the optimal number of clusters by plotting Within-Cluster Sum of Squares (WCSS).
Set the optimal number of clusters to K = 10 for finer segmentation.
Trained a K-Means model and assigned each customer to a cluster.
4. Model Evaluation & Insights
Silhouette Score was used to measure cluster quality and separation.
Customers were segmented into different groups based on behavior:
Loyal Customers: Frequent transactions and high coupon usage → Offer exclusive deals and VIP benefits.
High Spenders: Many transactions and quick coupon burns → Provide personalized recommendations and premium discounts.
Moderate Users: Occasional transactions and coupon burns → Use seasonal promotions to increase engagement.
Inactive Users: Low transaction activity and minimal coupon usage → Implement re-engagement campaigns and loyalty incentives.
