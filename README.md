
# 📊 Customer Churn Prediction System

## 📌 Project Overview
This project focuses on building an end-to-end Machine Learning classification model to predict customer churn for a telecommunications company. By analyzing historical customer demographics, account details, and service usage, the model identifies customers who are at high risk of leaving (churning), enabling the business to take proactive retention measures.

---

## 🎯 Problem Statement
Customer retention is critical for subscription-based businesses as acquiring new customers is significantly more expensive than retaining existing ones. The objective is to build a high-precision machine learning model that accurately classifies whether a customer will **Churn (1)** or **Remain (0)** based on their operational and service attributes.

---

## 📁 Dataset Description
* **Dataset Name:** Telco Customer Churn / Telecom Churn Dataset
* **Source:** Kaggle
* **Records:** 7,043 rows | 21 features
* **Target Feature:** `Churn` (Binary: Yes/No converted to 1/0)
* **Key Features:** `tenure`, `Contract`, `MonthlyCharges`, `TotalCharges`, `PaymentMethod`, `InternetService`, `OnlineSecurity`, `TechSupport`.

---

## 🛠️ Technologies Used
* **Programming Language:** Python 3.10+
* **Environment:** Kaggle Notebook / Jupyter Notebook
* **Data Processing:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn
* **Version Control:** Git, GitHub

---

## 🧹 Data Preprocessing
* **Missing Value Handling:** Replaced missing/blank spaces in `TotalCharges` with median values.
* **Duplicate Removal:** Checked and dropped duplicate records to avoid overfitting.
* **Categorical Encoding:** Applied One-Hot Encoding to multi-class categorical features (`Contract`, `PaymentMethod`, `InternetService`) and mapped binary categories (`Yes`/`No` -> `1`/`0`).
* **Feature Scaling:** Standardized numerical columns (`tenure`, `MonthlyCharges`, `TotalCharges`) using `StandardScaler`.
* **Data Splitting:** Split the preprocessed dataset into **80% Training set** and **20% Testing set** using stratified sampling.

---

## 📈 EDA Findings
1. **Contract Type:** Customers on **Month-to-month contracts** exhibit the highest churn rate compared to those on 1-year or 2-year contracts.
2. **Tenure Impact:** Churn probability is significantly higher during the **first 12 months** of customer tenure.
3. **Payment Method:** Electronic check users show a noticeably higher tendency to churn than auto-pay or credit card users.
4. **Charges:** Higher `MonthlyCharges` strongly correlate with increased customer churn.

---

## ⚙️ Features Used
* **Demographics:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* **Account Info:** `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`
* **Services:** `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`

---

## 🤖 Models Implemented
1. **Logistic Regression** (Baseline linear model)
2. **Decision Tree Classifier** (Tree-based non-linear model)
3. **Random Forest Classifier** (Ensemble bagging technique)

---

## 📊 Model Comparison & Evaluation Results

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | **0.7950** | **0.6120** | **0.6840** | **0.6460** |
| **Logistic Regression** | 0.7510 | 0.5340 | 0.7620 | 0.6280 |
| **Decision Tree** | 0.7240 | 0.4890 | 0.5210 | 0.5045 |

---

## 🏆 Best Model
* **Selected Model:** **Random Forest Classifier**
* **Reasoning:** It achieved the best overall metric balance, securing the highest **Accuracy (79.5%)** and **F1-Score (0.6460)**, effectively minimizing false positive predictions while maintaining strong recall capabilities on customer churn.

---

## 📊 Kaggle Results
* Complete exploratory workflow, data cleaning, model benchmarking, and visual confusion matrix evaluations were successfully executed within the Kaggle interactive GPU environment.
* **Kaggle Notebook Access:** Publicly shared and runnable end-to-end.

---

## 🚀 How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   cd your-repo-name

 * Install Required Libraries:
   pip install -r requirements.txt

 * Execute Notebook:
   Launch Jupyter Notebook or VS Code and run customer_churn_prediction.ipynb sequentially.
   jupyter notebook customer_churn_prediction.ipynb

📝 Conclusion
The Machine Learning workflow successfully identifies key indicators driving customer attrition—primarily short contract duration and high monthly charges. The Random Forest model provides reliable prediction metrics, giving business stakeholders a actionable solution to identify churn-prone customers and launch targeted retention campaigns.
