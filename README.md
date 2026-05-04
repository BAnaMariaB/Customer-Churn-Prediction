# Customer-Churn-Prediction
### **Introduction to the topic and motivation for the analysis**

Customer churn, is the phenomenon where customers terminate their relationship with a business or organization

 It is one of the most critical challenges facing the banking and financial services industry. "Churn prediction is used to identify customers who are about to leave a service provider. **It costs a
corporation 5 to 20 times more to keep a single customer than it does to acquire a new one**" (Sagala & Permai, 2021).

<br>

#### **Description of the purpose of the report**

This project aims to leverage **machine learning** and **statistical analysis** on a dataset of 10,000 bank customers. We want to **identify the key drivers of churn** and **build a predictive model capable of flagging at-risk customers** before they leave.

<br>

#### **Data used to perform the analysis**
Kaggle dataset :
https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction

* By **analyzing demographic factors** such as **age**, **geography**, and **gender** alongside behavioral and **financial indicators** like **account balance**, **number of products held**, and **activity status**, we seek to uncover actionable patterns that can inform targeted retention strategies.
* The insights derived from this analysis could enable the bank to proactively engage vulnerable customer segments, optimize resource allocation for retention campaigns, and ultimately reduce revenue loss.

#### **Problematique:** How can we accurately identify customers at risk of churning?

#### **Proposed Methodology**
1. Project Setup
2. EDA
3. Feature Engineering
4. Statistical Analysis
5. Modeling Comparison

#### **Statisticall Analysis**
After this analysis, our results are as follows:
* The dataset showed no critical missingness affecting the main variables used for analysis.
* We tested 3 features : age, customer activity and balance
* Statistical testing confirmed several significant differences between churned and non-churned customers:
    * Age: We are 95% confident that churned customers are between 8.52 and 9.48 years older, on average, than non-churned customers (observed ≈ 9.00 years, t = 30.42, p < 0.001).
    * Customer Activity: The association between activity status and churn was statistically significant (χ² = 242.99, p < 0.001). Inactive customers showed a substantially higher churn rate (26.9%) compared to active customers (14.3%), indicating that customer engagement is strongly linked to retention.
    * Balance: A Mann–Whitney test indicated that the distribution of account balances differs significantly between churned and non-churned customers (p < 0.001). Churned customers had a higher median balance (≈ 109,349) compared to non-churned customers (≈ 92,073), suggesting that higher-balance clients are more likely to leave.


#### **Model Analyses**
Model evaluation revealed a trade-off between predictive performance metrics.
* Logistic Regression achieved the highest recall (~78%), making it the most effective model for identifying churners, but at the cost of lower precision (~46%).
* Random Forest achieved higher overall accuracy (~85%) and precision (~70%), but with lower recall (~50%), indicating that it misses a larger proportion of churners.
* Further more a comparison between baseline and statistically refined models showed that removing non-significant features had minimal impact on performance,
