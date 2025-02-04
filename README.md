# Credit Risk Prediction

## 1. Objective
The objective of this project is to develop a machine learning model to predict the likelihood of a loan applicant defaulting. Financial institutions can use this model to assess credit risk, make informed lending decisions, and minimize financial losses.

## 2. Dataset
The project utilizes two datasets:
- **Application Data** – Contains demographic and financial information of loan applicants.
- **Bureau Data** – Contains previous credit records of applicants.
- Both datasets were merged to create a holistic dataset for credit risk assessment.

## 3. Approach & Methodology

### **Step 1: Data Collection & Preprocessing**
- Merged **Application Data** and **Bureau Data** for comprehensive analysis.
- Handled **missing values** using median imputation.
- Addressed **class imbalance** using **SMOTE (Synthetic Minority Over-sampling Technique)**.

### **Step 2: Exploratory Data Analysis (EDA)**
- Analyzed the distribution of the target variable (loan default).
- Identified correlations between financial indicators and credit risk.
- Examined the impact of key features like **income, loan amount, age, and education level**.
- **Visualizations:**
  - Bar chart showing class distribution.
  - Correlation heatmap of key features.
  - Age distribution vs. default rate.

### **Step 3: Feature Engineering & Selection**
- Created new variables, such as **AGE** (from DAYS_BIRTH).
- Standardized numerical features using **StandardScaler**.
- Selected important features using:
  - **Recursive Feature Elimination (RFE)**
  - **Feature Importance from Random Forest**

### **Step 4: Model Training & Evaluation**
- Trained the following machine learning models:
  - **Logistic Regression**
  - **Decision Tree**
  - **Random Forest**
- Evaluated models based on:
  - **Accuracy**
  - **Confusion Matrix**
  - **AUC-ROC Score**
  - **Precision-Recall Metrics**

### **Step 5: Hyperparameter Tuning & Best Model Selection**
- Used **GridSearchCV** and **RandomizedSearchCV** for hyperparameter tuning.
- Selected the best model based on **AUC-ROC Score**.
- Compared model performance before and after tuning.

### **Step 6: Business Insights & Recommendations**
#### **Top Important Features:**
1. **DAYS_BIRTH (Age-related feature)**
2. **AMT_CREDIT (Loan Amount)**
3. **NAME_EDUCATION_TYPE_Higher education**
4. **FLAG_OWN_CAR_Y (Owns a Car)**
5. **NAME_FAMILY_STATUS_Married**

#### **Business Recommendations:**
- Younger applicants show higher default rates; adjust lending policies accordingly.
- Use predictive credit scores in loan approval processes.
- Regularly update the model with new customer data for better predictions.

## 4. Conclusion
- Built a robust machine learning model to predict credit risk.
- **Best Model:** Logistic Regression (based on highest AUC-ROC after tuning).
- Insights can help financial institutions **optimize lending strategies** and **minimize financial losses**.

## 5. Technologies Used
- **Python** (pandas, numpy, matplotlib, seaborn, scikit-learn)
- **Machine Learning Algorithms** (Logistic Regression, Decision Tree, Random Forest)
- **SMOTE** (for handling class imbalance)
- **Hyperparameter Tuning** (GridSearchCV, RandomizedSearchCV)
  
