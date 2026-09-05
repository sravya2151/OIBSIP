# Wine Quality Prediction

## Project Overview

This project is part of the **OASIS INFOBYTE Data Analytics Internship – Level 2, Task 2**.

The objective of this project is to build and compare multiple machine learning classification models to predict wine quality categories using physicochemical properties of red wine.

The classification models used are:

* Random Forest Classifier
* SGD Classifier
* Support Vector Classifier (SVC)

---

## Dataset

The **Wine Quality dataset** was obtained from the **UCI Machine Learning Repository**.

The dataset contains **1,599 red wine samples** and **12 columns**, including physicochemical properties and the original wine quality score.

### Features

The following chemical properties were used as input features:

* Fixed acidity
* Volatile acidity
* Citric acid
* Residual sugar
* Chlorides
* Free sulfur dioxide
* Total sulfur dioxide
* Density
* pH
* Sulphates
* Alcohol

The original `quality` column contains wine quality scores ranging from 3 to 8.

---

## Data Loading

The dataset is stored as a semicolon-separated CSV file. Therefore, the dataset was loaded using:

```python
df = pd.read_csv("winequality-red.csv", sep=";")
```

---

## Exploratory Data Analysis

The dataset was inspected using:

* Dataset structure and data types
* Missing-value analysis
* Descriptive statistics
* Wine quality class distribution
* Chemical feature distributions
* Correlation analysis

### Class Imbalance

The original quality scores are highly imbalanced. Most wine samples belong to the middle quality scores, particularly 5 and 6, while scores such as 3 and 8 have very few observations.

This imbalance can cause classification models to favor the majority classes and perform poorly on minority classes. Therefore, accuracy alone may not provide a complete picture of model performance.

---

## Feature Engineering

The original quality scores were grouped into three broader categories:

| Quality Score | Category |
| ------------- | -------- |
| 3–4           | Low      |
| 5–6           | Medium   |
| 7–8           | High     |

This three-class approach reduces the effect of rare individual quality scores while preserving meaningful wine quality categories.

The original `quality` column was retained for reference, while `quality_class` was used as the classification target.

---

## Data Preprocessing

The dataset was divided into training and testing sets using an **80:20 split**.

A **stratified split** was used to maintain similar class proportions in both the training and testing datasets.

For SGD and SVC, the numerical features were standardized using `StandardScaler`.

Random Forest was trained using the original feature values because tree-based models do not require feature scaling.

---

## Machine Learning Models

Three classification algorithms were trained and evaluated.

### 1. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction performance and reduce overfitting.

### 2. SGD Classifier

The Stochastic Gradient Descent classifier is a linear classification algorithm that is efficient for training on numerical datasets.

### 3. Support Vector Classifier

SVC finds a decision boundary that separates different classes. An RBF kernel was used for this project.

---

## Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Classification Report
* Confusion Matrix

### Model Comparison

| Model          | Accuracy | Precision |   Recall | F1 Score |
| -------------- | -------: | --------: | -------: | -------: |
| Random Forest  | 0.859375 |  0.816848 | 0.859375 | 0.835419 |
| SGD Classifier | 0.825000 |  0.776012 | 0.825000 | 0.795656 |
| SVC            | 0.843750 |  0.794236 | 0.843750 | 0.809486 |

### Best Model

**Random Forest** achieved the best overall performance among the three tested models.

It achieved:

* **Accuracy:** 85.94%
* **Precision:** 81.68%
* **Recall:** 85.94%
* **F1 Score:** 83.54%

SVC achieved an accuracy of **84.38%**, while SGD Classifier achieved **82.50%**.

Therefore, Random Forest was selected as the most suitable model for deployment among the three evaluated models.

---

## Random Forest Feature Importance

Feature importance was calculated using the trained Random Forest model to identify which physicochemical properties contributed most to the classification predictions.

The feature importance visualization is included in the `images` folder.

---

## Visualizations

The project includes the following visualizations:

1. Wine quality distribution
2. Chemical feature distributions
3. Correlation heatmap
4. Random Forest confusion matrix
5. SGD confusion matrix
6. SVC confusion matrix
7. Random Forest feature importance
8. Model accuracy comparison

All visualizations are stored in the `images` folder.

---

## Project Structure

```text
DataAnalytics-L2-WineQualityPrediction/
│
├── images/
│   ├── quality_distribution.png
│   ├── chemical_features_distribution.png
│   ├── correlation_heatmap.png
│   ├── random_forest_confusion_matrix.png
│   ├── sgd_confusion_matrix.png
│   ├── svc_confusion_matrix.png
│   ├── random_forest_feature_importance.png
│   └── model_comparison.png
│
├── winequality-red.csv
├── Wine_Quality_Prediction.ipynb
├── requirements.txt
└── README.md
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## Conclusion

The project successfully demonstrated the use of machine learning classification techniques for wine quality prediction.

Among Random Forest, SGD Classifier, and SVC, **Random Forest achieved the highest accuracy and F1 score**, making it the preferred model for deployment in this project.

The results also show the importance of handling class imbalance and using appropriate evaluation metrics when working with classification datasets.

Future improvements could include hyperparameter tuning, cross-validation, class-weighting techniques, and evaluation using macro F1-score to better assess performance on underrepresented classes.

---

## Author

**Sravya Masimukku**

**Data Analytics Intern – OASIS INFOBYTE**

**Level 2 – Task 2: Wine Quality Prediction**
