# Vehicle Insurance Claim Fraud Detection
This project aims to create a model for predicting vehicle insurance claim fraud using data provided on [Kaggle](https://www.kaggle.com/shivamb/vehicle-claim-fraud-detection).

### Technologies
Python 3.10.12

## Exploratory Data Analysis (EDA)

The dataset contains 15420 rows and 33 columns. There are no missing values. Most variables are of type "object" or categorical.

Summary statistics are provided for numeric columns, showing the mean, standard deviation, minimum, maximum, and quartiles.

A count plot is generated to visualize the class distribution. There is a significant class imbalance.

## Data Visualization
Several visualizations are generated to explore relationships and patterns in the data. These include:
- Count plot showing the distribution of fraud cases by age for Female and Male

![image](https://github.com/aziegert/Vehicle_Insurance_Claim_Fraud_Detection/assets/123495041/b45087d2-5e05-465c-94bf-1366da4a861d)

- Pie chart showing claims by "Make"

![claims by Make](https://github.com/aziegert/Vehicle_Insurance_Claim_Fraud_Detection/assets/123495041/e7a00a8c-6d11-4195-aec5-b379175a99b3)

- Sunburst charts comparing fraud vs. non-fraud for features "BasePolicy" and "VehicleCategory"
![BasePolicy and VehicleCategory](https://github.com/aziegert/Vehicle_Insurance_Claim_Fraud_Detection/assets/123495041/b95475c8-8612-4f1c-a9b8-e899ccf174da)


## Data Preprocessing

Categorical ordinal features are transformed into ordered categorical data.

Categorical features like "Make", "MaritalStatus", "PolicyType", "VehicleCategory", and "BasePolicy" are one-hot encoded.


## Model Building
Three models are explored:
- XGBoost
- LightGBM
- CatBoost

The following metrics are used for evaluating model performance:
- F1
- Recall
- ROC AUC
- Precision
- Average Precision
- Accuracy

## Hyperparameter Tuning
In this project, it utilized a tool called Optuna for hyperparameter tuning. Optuna helps in finding the best configurations for models, leading to improved performance and better results.

## Shapley value – interpretability of the model
The first chart is a chart with a global interpretation. Cumulative SHAP values can demonstrate how much each feature contributed to predicting the target variable.

![Shap_f1_1](https://github.com/aziegert/Vehicle_Insurance_Claim_Fraud_Detection/assets/123495041/fcb011d6-d7f6-40b1-9cbe-440ca8633c58)

The graph below additionally shows the positive and negative relationships of feature values with the target variable.

![Shap_f1_2](https://github.com/aziegert/Vehicle_Insurance_Claim_Fraud_Detection/assets/123495041/da2d1dfa-e0c7-47ec-a979-885cd97fcfd4)
