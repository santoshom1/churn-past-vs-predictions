# churn-past-vs-predictions

## Overview
- Past data dashboard overview - [Click Here](https://public.tableau.com/app/profile/santhosh.kasam3498/viz/TelcoSQL/Dashboard1)
- Future predictions - [Click Here](https://public.tableau.com/app/profile/santhosh.kasam3498/viz/TelcoML/Dashboard1?publish=yes)
- ML model analysis - [Click Here](https://colab.research.google.com/drive/18dU0zT0SEvE1LV_me_7e-hX1ccMkxgaL?usp=sharing)

## 🧩 Project Summary

This project analyzes and predicts customer churn for a telecom company using a blend of SQL, Python (ML), and Tableau.
The workflow captures both historical insights (past churn patterns) and future predictions (churn probabilities), enabling data-driven customer retention strategies.

### 🔍 Dataset - [Click Here](https://drive.google.com/file/d/1PQeiKF3LzBJRb6C7oYS9gXgohaHcjHMz/view?usp=sharing)
**Records**: 7,043 customers
**Features**: 20+ customer attributes including tenure, contract type, internet service, payment method, and monthly charges.

**Key Columns**:

- customerID: Unique customer identifier
- Churn: Whether the customer left (Yes/No)
- MonthlyCharges: Billing per month
- Tenure: Duration with the company
- Contract, PaymentMethod, InternetService: Service-level details

## 🧮 SQL Analysis (Past Trends)

SQL queries were used for exploratory data analysis on the raw customer dataset to understand historical churn trends:

**Key Insights**:

- Month-to-month contract customers churn 3x more than long-term contracts.
- Electronic check payments have the highest churn rate (~45%).
- Customers with tenure <12 months are most at risk.
- Senior citizens and single-line subscribers show higher churn probability.

**Visuals**:
**Tableau Story 1** — “Customer Churn Analysis (SQL)”
👉 [Click Here](https://public.tableau.com/app/profile/santhosh.kasam3498/viz/TelcoSQL/Story1)

## 🤖 Machine Learning (Future Predictions)

Using Python (Scikit-learn), several models were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting

The model with the best recall score (**Gradient Boosting**) was selected to minimize missed churners.

**Model Output**:

- churn_probability: Likelihood of a customer churning

- churn_prediction: 1 → Predicted churn, 0 → Predicted stay

**Performance Metrics**:

- Accuracy: ~83%

- Recall (Churn Class): ~0.90

- Precision: ~0.83

## 📊 Tableau Dashboards
**Story 1 — Historical Churn Insights**
- SQL-based descriptive analysis

- Highlights churn patterns by demographics, contracts, and payment type

**Story 2 — Predictive Churn Risk**
- ML output visualized for business interpretation

- Displays churn probability, revenue at risk, and customer-level risk segmentation
  👉 [Click Here](https://public.tableau.com/app/profile/santhosh.kasam3498/viz/TelcoML/Dashboard1)


<img width="995" height="389" alt="image" src="https://github.com/user-attachments/assets/b8bc684a-b17e-46b5-b7af-df95840d90ca" />



**🧠 Insight**:

- The model’s predicted churn rate (~21.24%) aligns closely with historical patterns, indicating the model generalizes well.

- However, the predicted churn count (1,496) is slightly lower than the past actual churn (1,869), suggesting the model is slightly conservative — it prefers to avoid false alarms rather than over-predict churn.

## 💡 Business Recommendations

- Retention Focus: Prioritize high-value customers predicted to churn.

- Customer Incentives: Offer discounts or contract upgrades to month-to-month customers.

- Payment Optimization: Promote auto-pay and credit card methods over electronic checks.

- Early Engagement: Improve onboarding and engagement for customers with tenure <1 year.

- Continuous Monitoring: Update churn model monthly to capture behavioral shifts.
