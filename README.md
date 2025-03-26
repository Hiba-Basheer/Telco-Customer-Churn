**Customer Churn Prediction Project**

## **Project Overview**
This project focuses on predicting customer churn using machine learning techniques. The dataset used contains customer details, service subscriptions, and billing information. The primary objective is to build a classification model to identify customers who are likely to churn, allowing businesses to take preventive actions.

## **Dataset Details**
- **Dataset Size:** 7043 entries, 20 features
- **Target Variable:** `Churn` (0 - Not Churned, 1 - Churned)
- **Features:**
  - Categorical: `gender`, `Partner`, `Dependents`, `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`, `Contract`, `PaperlessBilling`, `PaymentMethod`
  - Numerical: `SeniorCitizen`, `tenure`, `MonthlyCharges`, `TotalCharges`

## **Data Preprocessing**
- **Handling Missing Values:** Checked for missing values and found none.
- **Encoding Categorical Variables:** Used `LabelEncoder` to convert categorical columns into numerical format.
- **Outlier Detection:** Conducted outlier analysis but found no significant outliers affecting model performance.
- **Feature Scaling:** Applied `StandardScaler` for numerical features to improve model efficiency.
- **Data Splitting:**
  - `train_test_split()` with `test_size=0.2` and `random_state=42`
  - 80% training data, 20% testing data

## **Model Training & Evaluation**
- **Machine Learning Model Used:** Logistic Regression (can be extended to other classifiers like Decision Tree, Random Forest, etc.)
- **Performance Metrics:**
  - **Accuracy:** 81.5%
  - **Precision:**
    - Class 0: 86%
    - Class 1: 68%
  - **Recall:**
    - Class 0: 90%
    - Class 1: 58%
  - **F1-Score:**
    - Class 0: 88%
    - Class 1: 62%
  - **Macro Average:** Precision: 77%, Recall: 74%, F1-score: 75%
  - **Weighted Average:** Precision: 81%, Recall: 82%, F1-score: 81%

## **Key Insights & Findings**
- The model has good accuracy but can be improved for better recall in predicting churned customers.
- Features like `tenure`, `Contract type`, and `MonthlyCharges` have a significant impact on churn.
- Customers with short tenure and month-to-month contracts are more likely to churn.
- Implementing additional models like Random Forest or Gradient Boosting can further enhance prediction performance.

## **Conclusion & Next Steps**
This project provides valuable insights into customer retention. Future improvements could involve:
- Using feature engineering techniques for better model interpretability.
- Implementing deep learning models for advanced pattern recognition.
- Deploying the model as an API for real-time predictions.

---
