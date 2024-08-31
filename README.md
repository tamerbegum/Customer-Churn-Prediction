Customer Churn Prediction
=========================

![Customer-Churn](https://github.com/user-attachments/assets/f78449b9-1310-4b83-9f57-44bff6c9902e)



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

## Final Model Testing
Tested the final model using the best-found parameters on the test set and evaluated its performance.

## Results
The Logistic Regression model was found to perform best, achieving the highest ROC AUC score during the model evaluation process. The model effectively predicts which customers are likely to churn based on the provided attributes.

## How to Run

### 1. Clone this repository:
1. Clone this repository: git clone https://github.com/yourusername/Customer-Churn-Prediction.git
2. Install the necessary dependencies using:
   ```bash
   pip install -r requirements.txt
