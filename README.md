
Bank-Customer-Churn-Analysis
The primary business objective of this project is to develop a machine learning model that accurately predicts customer churn for a bank. By identifying customers who are likely to churn, the bank can implement targeted retention strategies, enhance customer satisfaction, and ultimately increase profitability.

Machine Learning Model Documentation: Predicting Customer Churn for a Bank

Dataset

The bank customer churn data has 14 columns as follows:

RowNumber- Unique row number for each customer
CustomerId - Unique customer ID for each customer
Surname - Surname of the customer
CreditScore - Credit score of each customer
Geography - Location information of customers. There are three locations - Spain,France,Germany.
Gender - Male or Female
Age - Customer age
Tenure - How long the customer has been associated with the bank (in years)
Balance - Total balance in customer's account.
NumOfProducts - Total number of products purchased through the bank
HasCrCard - Whether the customer holds credit card or not.
IsActiveMember - Whether the customer is an active member of the bank or not
EstimatedSalary - Estimated salary of the customer
Exited - Whether the customer has exited from the bank or has stayed with the bank.
Methodology

Data Analysis and Preparation:

Exploratory Data Analysis (EDA)
Performed EDA to understand the data distribution and identified missing values. This step involved visualizing data through various plots and summarizing key statistics.
Encoding Categorical Variables
Converted categorical variables into numerical representations using techniques such as one-hot encoding or label encoding to make them suitable for machine learning algorithms.
Splitting the Dataset
Separated the dataset into features (X) and target variable (y). The target variable is the churn status of the customers.
Splitting into Training and Testing Sets
Split the dataset into training and testing sets to evaluate the model's performance on unseen data. A 70-30 split was used.
Resampling
Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique) to ensure the model does not become biased towards the majority class.
Feature Scaling
Standardized the features to ensure they have a mean of zero and a standard deviation of one. This step was crucial for algorithms that are sensitive to the scale of the data, such as logistic regression and K-nearest neighbors.
Model Building and Evaluation

1. Model Selection

Evaluated multiple classification algorithms to determine which one performs best for the churn prediction task. The models considered include:

Logistic Regression
K-Nearest Neighbors (KNN)
Decision Tree Classifier
Random Forest
Gradient Boosting
XGBoost
2. Performance Metrics

The following performance metrics were used to evaluate the models:

Precision: The ratio of true positive predictions to the total number of positive predictions.
Accuracy: The ratio of correctly predicted instances to the total number of instances.
Recall: The ratio of true positive predictions to the total number of actual positives.
F1-Score: The harmonic mean of precision and recall.
ROC AUC Score: The area under the Receiver Operating Characteristic curve, which measures the ability of the model to distinguish between classes.
3. Feature Importance

Identified the most important features contributing to the model's predictions using techniques such as feature importance scores.
Hyperparameter Tuning: Grid Search with Cross-Validation

Performed hyperparameter tuning using Grid Search with cross-validation to find the optimal parameters for the chosen models. This involved searching over a specified parameter grid and selecting the combination that maximizes model performance based on the ROC AUC score.
Results:

After testing six different machine learning models to predict customer churn, including Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, K-Nearest Neighbor, and XGBoost and after performing feature engineering and hyperparameter tuning we selected the XGBoost model having highest ROC-AUC value of 93% for final prediction.

image

Insights and Recommendations

Feature Insights
The most influential features identified by the model such as Age, EstimatedSalary, Balance, CreditScore, IsActiveMember, NumOfProducts, Tenure and Gender_Male should be analyzed to understand their impact on customer churn.
Targeted Retention Strategies
Use the model's predictions to develop targeted retention strategies. For instance, offering personalized incentives to high-risk customers or improving services in areas highlighted by important features.
Continuous Monitoring and Updating
Regularly update the model with new data to maintain its accuracy and relevance. Monitor the performance metrics to detect any degradation over time.
Customer Feedback Integration
Incorporate feedback from churned customers to refine the model further and address any underlying issues not captured by the current features.
By leveraging these insights, the bank can proactively address customer churn, thereby improving customer satisfaction and retention.
