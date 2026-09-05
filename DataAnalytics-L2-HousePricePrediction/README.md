# Predicting House Prices with Linear Regression

## Project Overview

This project focuses on predicting house prices using Machine Learning. A Linear Regression model was developed using the Ames Housing dataset from the Kaggle House Prices competition.

The project covers the complete machine learning workflow, including data exploration, data cleaning, feature selection, categorical encoding, model training, evaluation, visualization, and model comparison.

## Objective

The main objective is to build and evaluate a regression model that can predict house sale prices based on different characteristics of residential properties.

## Dataset

**Dataset:** House Prices - Advanced Regression Techniques
**Source:** Kaggle
**Dataset:** Ames Housing Dataset

The training dataset contains **1,460 houses** and **81 columns**, including the target variable `SalePrice`.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Workflow

### 1. Data Loading and Exploration

The dataset was loaded using Pandas and examined using:

* First few rows
* Dataset shape
* Data types
* Missing-value analysis
* Descriptive statistics

### 2. Exploratory Data Analysis

The distribution of the target variable `SalePrice` was visualized using a histogram with a KDE curve.

A correlation heatmap was also created to understand relationships between numerical variables and house prices.

### 3. Feature Selection

Important potential predictors of house prices were identified, including:

* `OverallQual`
* `GrLivArea`
* `YearBuilt`
* `GarageCars`
* `TotalBsmtSF`
* `1stFlrSF`
* `FullBath`
* `BedroomAbvGr`

Categorical variables such as `Neighborhood`, `HouseStyle`, and `KitchenQual` were also considered useful predictors.

### 4. Data Preprocessing

Missing values were handled using appropriate imputation strategies.

* Numerical features: median imputation
* Categorical features: most-frequent imputation
* Categorical variables: One-Hot Encoding

A Scikit-learn preprocessing pipeline was used to perform these operations consistently.

### 5. Train-Test Split

The dataset was divided into:

* **80% training data**
* **20% testing data**

A fixed random state of 42 was used to ensure reproducibility.

### 6. Linear Regression

A Linear Regression model was trained using Scikit-learn.

The model was evaluated using:

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

### 7. Model Visualization

The following visualizations were created:

* House price distribution
* Correlation heatmap
* Actual vs Predicted prices
* Residual plot
* Model comparison chart

### 8. Coefficient Analysis

The model coefficients were analyzed to identify features with strong positive and negative impacts on the predicted house price.

### 9. Ridge Regression - Bonus

Ridge Regression was implemented as an additional model.

Linear Regression and Ridge Regression were compared using MSE, RMSE, and R² score.

## Project Files

```text
DataAnalytics-L2-HousePricePrediction/
│
├── images/
│   ├── price_distribution.png
│   ├── correlation_heatmap.png
│   ├── actual_vs_predicted.png
│   ├── residual_plot.png
│   └── model_comparison.png
│
├── train.csv
├── House_Price_Prediction.ipynb
├── requirements.txt
└── README.md
```

## Results

The models were evaluated on the test dataset using MSE, RMSE, and R² score.

The comparison between Linear Regression and Ridge Regression is available in the notebook.

The model with lower MSE and RMSE and higher R² score provides better predictive performance on the test data.

## Conclusion

This project demonstrated an end-to-end machine learning workflow for house price prediction.

The process included data exploration, missing-value handling, categorical feature encoding, correlation analysis, train-test splitting, Linear Regression, model evaluation, residual analysis, coefficient interpretation, and Ridge Regression comparison.

The project helped demonstrate how machine learning can be applied to predict house prices from property characteristics and how different evaluation metrics and visualizations can be used to assess model performance.

## Author

**Sravya Masimukku**

Data Analytics Internship
OASIS INFOBYTE

````

Save the file.

### Step 30 — Check your folder

Your folder should now look like this:

```text
DataAnalytics-L2-HousePricePrediction
│
├── images
│   ├── price_distribution.png
│   ├── correlation_heatmap.png
│   ├── actual_vs_predicted.png
│   ├── residual_plot.png
│   └── model_comparison.png
│
├── train.csv
├── House_Price_Prediction.ipynb
├── requirements.txt
└── README.md
````

**Don't push to GitHub yet.** First tell me **“README done”**, and I'll take you through the final **GitHub upload/push step** carefully.
