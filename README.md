Customer Churn Prediction
=========================

Overview
--------
This project involves predicting customer churn based on various customer attributes and service details. The dataset is from Kaggle and includes information on customer behavior, service usage, account details, and demographics.

Dataset
--------
**Source:** Kaggle

**Description:**
The dataset aims to predict customer retention by analyzing various attributes and behaviors. Each row represents a customer with the following columns:

- **Churn:** Indicator of whether the customer left within the last month (target variable)
- **Services:** Types of services subscribed to (e.g., phone, internet, online security, etc.)
- **Account Information:** Details about customer tenure, contract type, payment method, monthly and total charges
- **Demographic Info:** Gender, age range, presence of partners, and dependents

**Objective:**
Develop predictive models to understand customer churn and create strategies to retain customers.

Code Overview
-------------
The script performs the following tasks:

1. **Import Libraries:**
   - Imports necessary libraries for data handling, visualization, and modeling.

2. **Load and Inspect Data:**
   - Reads the dataset from a CSV file and performs initial exploration.

3. **Preprocess Data:**
   - Identifies and processes categorical and numerical features.
   - Handles missing values and outliers.
   - Creates new features from existing data.

4. **Encoding:**
   - Applies label encoding to binary categorical features.
   - Uses one-hot encoding for other categorical features.

5. **Split Data:**
   - Divides the data into training, validation, and test sets.

6. **Model Training and Evaluation:**
   - Trains and evaluates multiple classification models including:
     - Logistic Regression
     - K-Nearest Neighbors (KNN)
     - Decision Tree Classifier
     - Random Forest Classifier
     - Gradient Boosting Classifier
     - AdaBoost Classifier
     - XGBoost Classifier
     - CatBoost Classifier
   - Uses GridSearchCV for hyperparameter tuning on Logistic Regression.
   - Each model is evaluated based on various metrics including ROC AUC, F1 score, Precision, Recall, and Accuracy. Performance is assessed using a validation set.
   - The ROC curve is plotted to visualize the model's ability to distinguish between positive and negative classes. The area under the ROC curve (AUC) is used to summarize the overall performance of the model.
   - The learning curve is plotted to visualize how the model's performance changes with the size of the training data. It helps in understanding if the model is overfitting or underfitting.


Instructions
------------
1. **Setup:**
   - Install the required libraries:
     ::
       pip install numpy pandas matplotlib seaborn scikit-learn catboost xgboost shap

2. **Data File:**
   - Place the `Telco-Customer-Churn.csv` file in the same directory as this script.

3. **Run the Script:**
   - Execute the script in your Python environment (e.g., Jupyter Notebook, PyCharm).

4. **Review Results:**
   - Check the output metrics and visualizations to assess model performance and feature importance.
