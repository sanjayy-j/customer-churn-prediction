# Customer Churn Prediction

## 📌 Problem Statement
Customer churn refers to customers leaving a service.  
The goal of this project is to analyze historical customer data and build machine learning models to predict whether a customer is likely to churn. Early identification of churn enables businesses to take preventive actions and improve retention.

---

## 📊 Dataset Overview
- Total customers: **7,043**
- Target variable: **Churn** (Yes / No)
- Features include:
  - Customer tenure
  - Contract type
  - Internet service
  - Monthly and total charges
  - Support and security services
  - Payment method

---

## 🔍 Level 1: Data Understanding & Exploratory Data Analysis (EDA)

### Data Cleaning
- Dropped `customerID` as it is a non-predictive identifier
- Converted `TotalCharges` from string to numeric
- Removed rows with invalid or missing values

### Exploratory Analysis
Visualizations were created to understand relationships between churn and key features:
- Churn distribution
- Tenure vs Churn
- Contract Type vs Churn
- Monthly Charges vs Churn

### Key Insights
- Dataset is imbalanced towards non-churn customers
- Customers with **shorter tenure** churn more frequently
- **Month-to-month contracts** show higher churn
- Higher **monthly charges** are associated with increased churn
- Long-term contracts and support services reduce churn risk

---

## 🤖 Level 2: Classical Machine Learning Models

### Models Trained
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVM)

### Evaluation Metrics
Each model was evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

### Observations
- Logistic Regression performed competitively and was easy to interpret
- Random Forest captured non-linear relationships but did not significantly outperform Logistic Regression
- SVM showed lower overall accuracy compared to other models

### Feature Importance
- Logistic Regression coefficients and Random Forest feature importance were analyzed
- Important features included:
  - Tenure
  - Contract type
  - Monthly and total charges
  - Internet service type
  - Payment method

---

## 🧠 Level 3: Neural Networks & Advanced Modeling

### Neural Network Model
- Implemented a feedforward neural network using Keras
- Used scaled input features
- Trained with binary cross-entropy loss and Adam optimizer

### Performance Comparison
The neural network achieved performance comparable to classical models but did not significantly outperform them, highlighting that:
- Classical models are strong baselines for structured tabular data
- Neural networks are not always superior for such problems

### Model Explainability (SHAP)
- SHAP (Shapley Additive Explanations) was used to interpret the neural network
- KernelExplainer was applied to handle the black-box nature of the model
- SHAP summary plots identified key drivers of churn:
  - Tenure
  - MonthlyCharges
  - TotalCharges
  - Contract duration
  - Internet service type

---

## 📈 Final Conclusion
- Customer churn can be effectively predicted using classical machine learning models
- Logistic Regression provided strong performance with high interpretability
- Neural networks matched but did not exceed classical models on this dataset
- Explainability techniques like SHAP are essential when using deep learning models

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- TensorFlow / Keras
- SHAP

---

## 📁 Repository Structure
customer-churn-prediction/
│
├── notebooks/
│ └── churn_analysis.ipynb
├── .gitignore
└── README.md

---

## 🚀 How to Run
1. Clone the repository
2. Install required dependencies
3. Open the notebook and run cells sequentially

---

## 📌 Notes
This project follows a structured, level-wise approach as required and emphasizes correct workflow, evaluation, and interpretability over model complexity.
