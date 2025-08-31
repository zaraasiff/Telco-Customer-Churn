📊 Telecom Customer Churn Prediction

📌 Objective
The objective of this project is to predict **customer churn** for a telecom company using machine learning.  
We build an end-to-end pipeline including **data preprocessing, model training, evaluation, and interpretability**.  
The project helps stakeholders **identify at-risk customers** and take **preventive actions** to improve retention.



📂 Dataset
- Source: [Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- Size: 7,043 customers  
- Features:  
  - Demographics (gender, senior citizen, dependents)  
  - Account info (tenure, payment method, contract type)  
  - Services signed up (internet, phone, streaming, etc.)  
  - **Target variable:** `Churn` (Yes/No)

---

⚙️ Data Preprocessing
- ✅ Missing values handled (e.g., replacing `NaN` in TotalCharges)  
- ✅ Categorical features encoded using **Label Encoding & One-Hot Encoding**  
- ✅ Numerical features scaled with **StandardScaler**  
- ✅ Class imbalance addressed using **SMOTE (Synthetic Minority Oversampling Technique)**  



🤖 Models Used
We trained and compared **3 ML models**:

1. **Logistic Regression**  
   - Simple linear model  
   - Highly interpretable  

2. **Random Forest Classifier**  
   - Ensemble of decision trees  
   - Handles non-linearity and feature interactions  

3. **XGBoost Classifier**  
   - Gradient boosting algorithm  
   - Most accurate & robust in tests  

📈 **Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score  

---

🔍 Model Interpretability (SHAP)
- Used **SHAP (SHapley Additive exPlanations)** to interpret predictions  
- Identified **top drivers of churn** (Tenure, Contract Type, Monthly Charges, Tech Support)  
- Generated **feature impact plots** for explainability  

---

📈 Findings
- **XGBoost performed best** with highest accuracy and F1-score  
- Key churn drivers:  
  - Short Tenure (new customers leave faster)  
  - Month-to-Month Contracts (less stable customers)  
  - High Monthly Charges (pricing dissatisfaction)  
  - Lack of Tech Support (service dissatisfaction)  

---

🎯 Business Insights
- Offer **discounts/loyalty rewards** to long-term customers  
- Promote **annual/2-year contracts** for stability  
- Provide **better technical support** to reduce dissatisfaction  
- Monitor **high-spending customers** for churn risk  

  
🗂️ Project Structure
 data                # Dataset (Telco Customer Churn)
  └── Telco-Customer-Churn.csv
notebooks/           # Jupyter/Colab notebooks
  └── churn_analysis.ipynb
 scripts/             # Python scripts for preprocessing & modeling
  └── preprocessing.py
   └── model_training.py
models/              # Saved trained models (pkl files)
  └── xgboost_model.pkl
 insights/            # Insight card & visualizations
  └── insight_card.png
README.md            # Project documentation
  └── requirements.txt     # List of Python libraries required


