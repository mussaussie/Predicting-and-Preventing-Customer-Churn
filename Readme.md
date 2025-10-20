# 📊 AI-Driven Insights: Predicting and Preventing Customer Churn

![Dashboard Overview](/Screenshot%202025-10-20%20122844.png)

---

## 🧠 Project Overview
This project demonstrates how **Machine Learning** and **Business Intelligence (BI)** work together to predict and prevent customer churn in the telecommunications industry.  
It combines **supervised ML modeling** (Logistic Regression & Random Forest) with **Tableau visualization** to uncover insights that directly support business decision-making.

The project focuses on applying **end-to-end data science fundamentals** — from data cleaning, feature engineering, and modeling to business interpretation and deployment.

---

## 🎯 Objective
- Predict the probability of customer churn using ML classification models  
- Identify the most important churn drivers using feature importance  
- Compare model performance (Logistic Regression vs Random Forest)  
- Build a Tableau dashboard for leadership decision-making  
- Demonstrate how to **deploy the model** on new unseen customer data  

---

## 🧩 Dataset
**Source:** [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/blastchar/telco-customer-churn)  
**Rows:** ~7,000  
**Columns:** 20+ customer and service-related attributes  

### Main Features:
- **Demographics:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- **Services:** `PhoneService`, `InternetService`, `TechSupport`, `StreamingTV`
- **Account Info:** `Contract`, `PaymentMethod`, `tenure`, `MonthlyCharges`, `TotalCharges`
- **Target Variable:** `Churn` (Yes / No)

---

## 🧹 Data Preprocessing
1. **Handled missing values** in `TotalCharges`
2. **Converted categorical features** using one-hot encoding
3. **Scaled numerical columns** for Logistic Regression
4. **Split data** into training (80%) and testing (20%)

---

## 🧮 Machine Learning Models

### 🔹 Logistic Regression
- Interpretable baseline model  
- Captures linear relationships  
- Accuracy: **78.5%**
- ROC-AUC: **0.69**

### 🔹 Random Forest Classifier
- Handles non-linear and interaction effects  
- Provides feature importance  
- Accuracy: **78.8%**
- ROC-AUC: **0.68**

| Model | Accuracy | F1 Score | Precision | Recall | ROC-AUC |
|--------|-----------|-----------|------------|----------|-----------|
| Logistic Regression | 0.785 | 0.55 | 0.62 | 0.49 | 0.692 |
| Random Forest | 0.788 | 0.55 | 0.63 | 0.48 | 0.689 |

---

## 🔍 Model Insights

### 📈 Feature Importance (Random Forest)
![Feature Importance](/output.png)

**Top churn drivers:**
1. **Tenure** — Customers with shorter tenure are more likely to leave  
2. **MonthlyCharges** — High bills strongly correlate with churn  
3. **TotalCharges** — Customers paying more overall have higher churn risk  
4. **Contract Type** — Month-to-month customers are the most unstable segment  

---
.

---

## ⚙️ Model Deployment & Real-World Implementation

The dataset we trained on **includes known churn outcomes**, allowing the model to learn churn patterns.  
Once trained, this model can be **deployed to predict churn on new data** — where churn is *unknown*.

### 🔄 Real-World Process:
1. **Input New Customer Data:**  
   Feed in active customer records without the `Churn` column.
2. **Model Predicts Churn Probability:**  
   Example output → `CustomerID | Tenure | Contract | Predicted_Prob`
3. **BI Integration:**  
   Send these probabilities into Tableau or a CRM dashboard.
4. **Action:**  
   Marketing focuses on customers with `Predicted_Prob > 0.6`.

| CustomerID | Tenure | MonthlyCharges | Contract | Predicted_Prob | Action |
|-------------|---------|----------------|-----------|----------------|--------|
| C001 | 2 | 85.5 | Month-to-month | 0.92 | Send retention offer |
| C002 | 30 | 25.3 | Two-year | 0.10 | Stable – no action |
| C003 | 8 | 70.1 | One-year | 0.65 | Follow-up call |

> ✅ This makes the model **preventive**, not just analytical — helping businesses act *before* customers leave.

---

## 💼 Business Impact

| Business Challenge | ML + BI Solution |
|--------------------|------------------|
| High customer churn | Predict churn likelihood for each customer |
| Marketing inefficiency | Focus campaigns only on high-risk segments |
| Lack of insight | Identify service and billing features that cause churn |
| Poor retention planning | Recommend personalized offers & contract types |

### 🚀 Strategic Benefits:
- Reduce churn → increase recurring revenue  
- Optimize marketing spend  
- Increase customer lifetime value (CLV)  
- Enable proactive customer engagement  

---

## 💡 Recommendations
* Focus on **short-tenure** and **month-to-month** customers  
* Offer **loyalty discounts** for the first 6 months  
* Encourage **annual contracts** with better pricing  
* Target **high MonthlyCharges** customers with retention rewards  

---

## 🧠 Handling the “Not Perfect Model” Question

If asked, “Why isn’t your model perfectly accurate?”:

> In business reality, perfect prediction is impossible because customer churn is influenced by unrecorded human factors (mood, competitors, personal life).  
> Instead of aiming for 100% accuracy, our goal is **consistent, explainable prediction** that segments customers into actionable risk groups.  
> The 78% accuracy gives enough reliability to guide retention strategies without overfitting or bias.

---

## 🧠 Handling the “How Does It Help the Business” Question

> This project transforms raw data into **decisions**.  
> By predicting who is likely to churn and why, managers can:  
> - Prioritize retention campaigns  
> - Personalize offers  
> - Reduce churn rate by up to 15–20%  
> - Improve customer experience and lifetime value  

It shows clear ROI and connects **AI with strategic leadership** decisions.

---

## 🚀 Tools & Technologies
- **Python:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **Tableau:** Dashboard and storytelling visualization  
- **Jupyter Notebook:** Data cleaning, modeling, evaluation  

---
## 🧾 Future Work
- Integrate **SHAP explainability** for better interpretability  
- Deploy as **Flask or Streamlit web app**  
- Automate CRM integration for real-time churn scoring  

---

## 🧑‍💻 Author
**Abdul Mussavir**  
📍 Adelaide, Australia  
📧 [mussaussie@gmail.com](mailto:mussaussie@gmail.com)  
💼 Data Analyst | Data Science & Machine Learning Enthusiast  

---

### 🏆 Summary
> *This project bridges data science and business strategy — turning churn prediction into a proactive retention management system.*


