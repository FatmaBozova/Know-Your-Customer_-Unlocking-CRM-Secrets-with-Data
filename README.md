🔍 Know Your Customer: Unlocking CRM Secrets with Data

This project aims to analyze customer purchasing behavior using RFM analysis, segmentation, clustering, and purchase propensity modeling. 
The data comes from an online retail dataset containing transaction-level records.

📂 Dataset Overview

Source: Online Retail Excel DatasetRows: ~500,000+ transactionsFeatures include:
InvoiceNo, StockCode, Description, Quantity
InvoiceDate, UnitPrice, CustomerID, Country

🔧 Project Workflow

1. Data Exploration and Preprocessing
  Loaded Excel data and explored structure
  Removed null values and converted CustomerID to string
  Treated outliers in Quantity and UnitPrice using IQR clipping
  Created a new column: Total_Price = Quantity * UnitPrice
  Visualized sales trends and customer distribution
  Generated WordClouds for customer counts and revenue by country

2. RFM Analysis & Segmentation
  Created recency, frequency, monetary metrics
  Scored each metric from 1 to 5
  Generated RF_SCORE and mapped segments:
  Champions, Loyal Customers, Hibernating, At Risk, etc.
  Visualized segment distribution in 3D with Plotly
  Summarized average metrics per segment

3. Segment Strategy Insights

  Champions: Highly active, strong cross-sell potential
  Loyal Customers: High frequency, moderate spenders — ideal for retention
  Need Attention: High monetary value, low recency — target with coupons/bonuses
  Can't Lose: High frequency but inactive — re-engagement campaigns recommended
  Hibernating: Long inactive — target via reactivation strategies (email, social media)

📊 Clustering Analysis

K-Means Clustering

  Scaled recency, frequency, monetary with StandardScaler
  Determined optimal k using Elbow Method and Silhouette Score (best at k=4)
  Visualized clusters in 3D
  Segment Interpretations
  Cluster 0: Regular shoppers, high spenders
  Cluster 1: Infrequent shoppers with high total spend
  Cluster 2: Moderate spend and frequency
  Cluster 3: Newcomers, low spenders

🤖 Purchase Propensity Modeling

  Defined label: customers with recency <= 30 and monetary >= 250 as likely to purchase next month
  Features: Recency_Score, Frequency_Score, Monetary_Score
  Model: Logistic Regression

Evaluation:

  Accuracy, Confusion Matrix, Classification Report
  ROC Curve with AUC ≈ 0.93 (high performance)

🔍 Behavioral Grouping

  Grouped customers by recency, frequency, monetary bins
  Calculated average purchase likelihood (Purchase_Next_Month)
  Categorized purchase trend:
  High Trend: ≥ 0.7
  Medium Trend: 0.3–0.69
  Low Trend: < 0.3
  Merged with RFM data to assign each customer a purchase tendency category

✅ Summary

  Cleaned and explored real-world retail data
  Performed full RFM and segment mapping
  Applied clustering and machine learning classification
  Identified actionable strategies based on customer profiles

💾 Deliverables

Final Jupyter Notebook
WordCloud and sales visualizations
3D segment and cluster visualizations
Trained logistic regression model

👩‍💻 Author

Fatma BozovaEmail: turannfatma@gmail.comLinkedIn: linkedin.com/in/fatma-bozovaGitHub: github.com/FatmaBozova

