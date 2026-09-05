# Fraud Detection Using Machine Learning

## Project Overview

This project focuses on detecting fraudulent financial transactions using machine learning techniques. The dataset contains highly imbalanced transaction data, making fraud detection a challenging classification problem.

The project explores the data, handles class imbalance using SMOTE, trains multiple machine learning models, and evaluates them using fraud-focused performance metrics.

## Objectives

* Analyze the highly imbalanced transaction dataset.
* Perform exploratory data analysis (EDA).
* Analyze transaction amounts and time-of-day patterns.
* Explain why accuracy can be misleading for imbalanced fraud datasets.
* Handle class imbalance using SMOTE.
* Train Logistic Regression and Random Forest models.
* Evaluate models using Precision, Recall, F1-Score, and ROC-AUC.
* Analyze Random Forest feature importance.
* Discuss scalability for high-volume transaction processing.

## Dataset

The project uses the **Credit Card Fraud Detection** dataset.

The dataset contains:

* 284,807 transactions
* 30 input features
* 1 target variable (`Class`)
* 492 fraudulent transactions
* Approximately 0.17% fraudulent transactions

The `Class` column represents the target:

* `0` → Legitimate transaction
* `1` → Fraudulent transaction

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* Jupyter Notebook

## Machine Learning Workflow

1. Load the dataset.
2. Inspect the dataset structure and statistics.
3. Analyze class imbalance.
4. Perform exploratory data analysis.
5. Split the data using stratified train/test splitting.
6. Scale the features.
7. Apply SMOTE to the training data.
8. Train Logistic Regression.
9. Train Random Forest.
10. Evaluate model performance.
11. Plot confusion matrices.
12. Plot ROC-AUC curves.
13. Analyze feature importance.
14. Discuss scalability and business considerations.

## Model Performance

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression |   0.9741 |    0.0578 | 0.9184 |   0.1088 |  0.9708 |
| Random Forest       |   0.9995 |    0.8710 | 0.8265 |   0.8482 |  0.9685 |

### Model Selection

Random Forest was selected as the preferred overall model because it provides a much better balance between precision, recall, and F1-score.

Logistic Regression achieved higher recall, detecting 91.84% of fraudulent transactions, but its very low precision resulted in many false-positive alerts.

Random Forest achieved 87.10% precision and 82.65% recall, providing a stronger overall balance for practical fraud detection.

## Why Accuracy Is Not Enough

The dataset is extremely imbalanced, with only about 0.17% fraudulent transactions.

A model could predict almost every transaction as legitimate and still achieve very high accuracy while failing to detect fraud.

Therefore, Precision, Recall, F1-Score, and ROC-AUC are more informative metrics for this problem.

Recall is particularly important when the cost of missing fraudulent transactions is high. However, precision must also be monitored to prevent excessive false-positive alerts.

## Feature Importance

Random Forest feature importance was used to identify the features that contributed most to the model's predictions.

The feature importance visualization is available in:

`images/feature_importance.png`

## Project Visualizations

The project includes the following visualizations:

* `class_distribution.png`
* `transaction_amount_distribution.png`
* `time_of_day_analysis.png`
* `confusion_matrix_logistic_regression.png`
* `confusion_matrix_random_forest.png`
* `roc_curve.png`
* `feature_importance.png`
* `model_comparison.png`

## Scalability

A production fraud detection system may need to process approximately 1 million transactions per hour.

For this scale, the machine learning model could be integrated with:

* Real-time data streaming
* Distributed processing
* Parallel model serving
* Efficient feature engineering pipelines
* Model monitoring
* Data drift detection
* Periodic model retraining
* Threshold optimization

Technologies such as Apache Kafka, Apache Spark, or Apache Flink could be considered for large-scale transaction processing.

## Conclusion

This project demonstrates an end-to-end machine learning approach for fraud detection in a highly imbalanced dataset.

SMOTE was used to address class imbalance during model training, while stratified splitting ensured that the test set retained the original class distribution.

Two models were evaluated, and Random Forest provided the best overall balance of precision, recall, and F1-score.

The project highlights that successful fraud detection requires more than high accuracy. Recall, precision, F1-score, ROC-AUC, threshold selection, and scalability are important considerations for building a practical fraud detection system.
