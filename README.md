# Customer Churn Prediction

Predicting customer churn is a crucial task for businesses to retain customers and reduce revenue loss. This project analyzes customer data and uses machine learning models to predict whether a customer will leave a company or continue using its services.

---

## **Project Objective**

- Clean and preprocess customer data
- Perform Exploratory Data Analysis (EDA) to extract insights
- Encode categorical features and scale numerical features
- Train multiple machine learning models: Logistic Regression, Decision Tree, Random Forest
- Compare model performance and select the best model for churn prediction
- Evaluate feature importance to identify key factors influencing churn

---

## **Dataset**

- <a href="https://github.com/Akshataa28/Customer-Churn-Prediction-ML/blob/main/churn.csv">Churn.csv</a>
- Total records: 7043
- Columns: 21 (customer demographic, account, and usage information)


---

## **Tools & Technologies**

- **Programming:** Python 3.x
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Joblib
- **Machine Learning Concepts:** Classification, Feature Engineering, Hyperparameter Tuning, Cross-Validation

---

## **Project Workflow**

1. **Data Loading & Inspection**
   - Loaded dataset using Pandas
   - Checked for null values and data types
   - Converted `TotalCharges` to numeric and handled missing values

2. **Exploratory Data Analysis (EDA)**
   - Visualized categorical features vs. churn
   - Analyzed numeric features using boxplots and correlation heatmaps
   - Identified trends:  
     - Month-to-month contracts and fiber optic internet users had higher churn  
     - Customers with higher monthly charges were more likely to churn

3. **Data Preprocessing**
   - Label encoding for binary columns (`Yes`/`No`)
   - One-hot encoding for multi-category columns (`Contract`, `PaymentMethod`, etc.)
   - Standard scaling of numeric features

4. **Model Training & Evaluation**
   - **Logistic Regression**  
     - Train Accuracy: 75\%, Test Accuracy: 74\%
   - **Decision Tree**  
     - Train Accuracy: 75\%, Test Accuracy: 73.8\%
   - **Random Forest (Best Model)**  
     - Test Accuracy: 76.4\%, Recall (Churn=1): 77\%, F1-score: 0.64

5. **Hyperparameter Tuning**
   - Tuned Random Forest parameters using GridSearchCV
   - Final model parameters: `max_depth=6`, `min_samples_split=5`, `n_estimators=200`
   - Tuned model accuracy: 74.7\%, CV Mean: 75.6\%

6. **Feature Importance**
   - Top factors influencing churn:
     - `Contract` type
     - `MonthlyCharges`
     - `tenure`
     - `PaymentMethod`
     - Online services usage (StreamingTV, TechSupport, etc.)

7. **Model Saving**
   - Saved final model and preprocessing objects for future predictions:
     - `Churn_model.pkl`
     - `Scaler.pkl`
     - `model_columns.pkl`

---

## **Folder Structure**
