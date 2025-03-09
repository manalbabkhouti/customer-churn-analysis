# customer-churn-analysis

🔥 Customer Churn Prediction - Full Analysis & Insights

📚 Project Overview

Customer churn is a critical challenge for businesses. This project aims to predict which customers are likely to leave using machine learning models and derive actionable insights that can help reduce churn.

✨ Key Objectives

- Understand the factors leading to churn through data analysis.

- Compare multiple machine learning models to find the best one for prediction.

- Provide business insights based on the model findings.

- Recommend strategies to reduce churn.

📂 Dataset Overview

Rows: ~10,000 customers

Target Variable: Attrition_Flag (1 = Churner, 0 = Non-Churner)

Features:

- Demographic Data: Customer_Age, Gender, Dependent_count

- Account History: Months_on_book, Total_Relationship_Count, Months_Inactive_12_mon

- Transaction Behavior: Total_Trans_Amt, Total_Trans_Ct, Credit_Limit

- Financial Metrics: Total_Revolving_Bal, Avg_Utilization_Ratio


📊 Exploratory Data Analysis (EDA)

🌟 Key Findings from Data Exploration

- Churn Rate: ~16% of customers have churned.

- Customer Age Distribution: Majority are between 40-60 years old.

- Credit Limit: Higher limits are associated with lower churn.

- Total Transactions: Customers with fewer transactions are more likely to churn.

- Inactive Months: Churners tend to have more inactive months in the last year.

- Utilization Ratio: Customers who churn tend to have a higher utilization ratio, suggesting they are maxing out their credit.


🔍 Visualizations & Insights

- Churn vs. Transactions: Customers with low transaction count are at a high risk of churning.

- Churn vs. Credit Limit: Churners tend to have lower credit limits.

- Churn vs. Relationship Duration: Longer relationships with the bank tend to have lower churn.

🔧 Conclusion: The main drivers of churn are low transaction activity, high utilization ratio, and recent inactivity.


🌀 Feature Engineering

✅ Steps Taken

- One-Hot Encoding for categorical variables (Gender, Education_Level, etc.).

- Standardization for numerical variables (Credit_Limit, Total_Trans_Amt, etc.).

- Outlier Handling: Identified extreme values in transaction amounts and credit limits but kept them to retain useful information.

- Feature Importance Analysis to determine key predictors.


📊 Model Evaluation & Selection

Several machine learning models were trained and tested for churn prediction. Below is a summary of their performance:

- Logistic Regression achieved 88.75% accuracy but struggled with recall for churners (48%). While simple, it was not the best choice for detecting churn.

- Random Forest performed well, capturing patterns effectively with 95.41% accuracy and 77% recall for churners.

- XGBoost delivered strong performance with 96.79% accuracy and 87% recall, showing a great balance between precision and recall.

- LightGBM (Optimized) emerged as the best model with 97.19% accuracy and 88% recall, making it the fastest and most accurate option.

- MLP (Neural Network) struggled with structured data, achieving only 84.65% accuracy and a 15% recall for churners.

- SVM completely failed to detect churners, with 83.96% accuracy but 0% recall for churners, making it unsuitable for this problem.

🎡 Final Model Choice

After comparing all models, LightGBM was selected as the best model due to its high accuracy, speed, and ability to detect churners effectively. While XGBoost also performed well, LightGBM slightly outperformed it in speed and recall. Random Forest was reliable but slightly weaker than LightGBM. Deep learning approaches like MLP and SVM were not effective for this structured dataset.

🔧 Feature Importance - Key Factors Influencing Churn

To understand what drives customer churn, LightGBM Feature Importance Analysis was conducted. The most critical factors influencing churn were:

- Total_Trans_Amt - The total amount of transactions in the last year was the most significant predictor of churn.

- Total_Amt_Chng_Q4_Q1 - The change in transaction amount between Q4 and Q1 strongly influenced churn likelihood.

- Total_Trans_Ct - The total number of transactions played a key role, with fewer transactions correlating to higher churn.

- Total_Ct_Chng_Q4_Q1 - Changes in the number of transactions over time were also a strong indicator.

- Customer Age - Older customers tended to have different churn patterns.

- Total Revolving Balance - Higher revolving balances were associated with increased churn risk.

🔍 Key Insight: Customers who spend less, have fewer transactions, and show reduced activity are at the highest risk of churning.

🔄 Hyperparameter Tuning & Optimization

To improve model performance, GridSearchCV was used to fine-tune LightGBM hyperparameters. This resulted in an optimized accuracy of 97.19%, making it the most effective model for churn prediction.

💡 Business Recommendations

Based on the findings, the following strategies are recommended to reduce churn and improve customer retention:

1️⃣ Increase Engagement for Low-Transaction Users

- Offer personalized promotions to inactive customers.

- Implement transaction alerts if a customer's activity drops significantly.

2️⃣ Credit Limit Adjustments

- Customers with low credit limits are at a higher risk of churning.

- Providing credit limit increases to responsible customers may help in retention.

3️⃣ Loyalty Programs

- Encourage long-term customer relationships through exclusive rewards.

- Offer cashback incentives to boost transaction frequency.

🔄 Future Improvements

To further enhance the model and business insights, future work could include:

- Exploring deep learning models with a larger dataset.

- Deploying the model as an API for real-time churn predictions.

- Using unsupervised learning techniques like clustering to identify hidden customer segments with different churn patterns.


💪 This project successfully identified key churn predictors, selected the best-performing model, and provided actionable business recommendations. Ready for deployment and further improvements! 🚀




👤 Author

👤Manal Babkhouti
📧Email: babkhoutimanal@gmail.com
🔗GitHub: manalbabkhouti 
🔗LinkedIn: https://www.linkedin.com/in/manal-babkhouti-63b6b722a

