# Customer Churn Prediction

## 📌 Problem Statement
Customer churn refers to customers leaving a service.  
The objective of this project is to use historical customer data to predict whether a customer is likely to churn, enabling businesses to take preventive action.

---

## 📊 Dataset
- Total customers: 7,043
- Target variable: `Churn` (Yes / No)
- Data includes:
  - Customer tenure
  - Internet services
  - Contract type
  - Payment method
  - Monthly and total charges

---

## 🧹 Data Preprocessing
- Removed `customerID` as it is a non-predictive identifier
- Converted `TotalCharges` from text to numeric
- Handled missing values
- Encoded categorical variables using one-hot encoding
- Encoded target variable (`Churn`) as binary (0 = No, 1 = Yes)

---

## 🤖 Modeling
- Baseline model: **Logistic Regression**
- Train–test split: 80/20
- Stratified sampling to handle class imbalance

---

## 📈 Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score

**Why not accuracy alone?**  
Churn is an imbalanced problem, so recall and F1-score are more informative.

---

## 🔍 Results (Baseline Logistic Regression)
- Accuracy: ~79%
- Churn recall: ~53%
- Indicates reasonable baseline performance with scope for improvement

---

## 🚀 Future Improvements
- Improve recall using class-weighted models
- Compare with Random Forest and SVM
- Add explainability using SHAP
- Build an end-to-end churn prediction pipeline

---

## 🛠️ Tools Used
- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook
