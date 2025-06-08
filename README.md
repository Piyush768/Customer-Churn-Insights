# 📊 Customer Churn Analysis and Segmentation for Subscription-Based Services

## 🔍 Problem Statement

Churn is a critical problem for subscription-based services, especially in competitive sectors like telecom. This project aims to:
- Identify customers likely to churn
- Uncover key churn drivers
- Segment customers based on usage and value
- Recommend personalized retention strategies

---

## 🎯 Objectives

- Predict which customers are likely to leave
- Understand factors influencing churn behavior
- Segment customers to enable targeted marketing and retention strategies
- Improve customer lifetime value and profitability

---

## 🧠 Key Questions Answered

- Which features (e.g., Monthly Revenue, Contract Type, Customer Care Calls) predict churn?
- How do usage patterns vary by segment?
- Which segments are at high risk, and which are loyal or high-value?

---

## 🧾 Dataset

- **Rows**: 51,047
- **Columns**: 58
- Key features include: Monthly Revenue, Minutes, Churn, Total Recurring Charges, Customer Care Calls, Roaming, and Demographics

---

## 🧼 Data Preprocessing

- Missing values removed (<0.7%)
- Outliers detected via IQR method
- Label encoding and One-Hot encoding applied to categorical features
- RobustScaler used for normalization
- SMOTE used to address class imbalance

---

## 📊 Exploratory Data Analysis

- Churn distribution
- Revenue and minutes vs. churn visualizations
- Usage behavior trends over months
- Pair plots of key features
- Scatter plots for revenue vs. recurring charges by churn status

---

## 📑 Customer Segmentation

Using features like revenue, usage, and device count:
1. **High-Value, Heavy Users** – Offer loyalty programs, premium plans
2. **Moderate Users** – Upsell through tailored promotions
3. **Low Usage, High Devices** – Promote family/group plans
4. **Low Engagement** – Use cost-effective retention strategies

---

## 🤖 Machine Learning Models

| Model                        | Accuracy | Best Recall (Churned) | Notes                              |
|-----------------------------|----------|------------------------|-------------------------------------|
| Random Forest (SMOTE)       | 0.69     | 0.24                   | Good for non-churned                |
| Logistic Regression (SMOTE) | 0.53     | 0.61                   | Best for churned customers          |
| XGBoost (SMOTE)             | 0.71     | 0.18                   | High accuracy, low recall (churned) |
| LightGBM (SMOTE)            | **0.72** | 0.15                   | Best accuracy overall               |
| CNN Model                   | 0.72     | 0.02                   | Biased toward majority class        |

---

## 🧠 Feature Selection

Lasso selected the following features:
- Monthly Minutes
- Total Recurring Charge
- Average Minutes
- PercChange Minutes
- Unique Subs
- Credit Rating

---

## 🛠️ Tools & Libraries

- Python (Pandas, NumPy, Scikit-learn)
- SMOTE (Imbalanced-learn)
- LightGBM, XGBoost, Random Forest
- Matplotlib & Seaborn
- TensorFlow/Keras (CNN model)

---

## 📈 Business Impact

- Enables telecom companies to reduce churn through proactive engagement
- Helps in customizing plans and communication for different customer types
- Enhances long-term customer satisfaction and profitability

---
