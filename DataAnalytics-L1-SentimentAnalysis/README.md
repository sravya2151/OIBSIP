# OIBSIP Data Analytics – Sentiment Analysis

## Project Overview

This project was completed as part of the Oasis Infobyte Data Analytics Internship.

The objective of this project is to build a machine learning model that classifies movie reviews according to their sentiment.

The IMDb Movie Reviews dataset was used for this project. The dataset contains 50,000 labeled movie reviews divided into positive and negative sentiment classes.

## Dataset

The dataset contains:

* 50,000 movie reviews
* 25,000 positive reviews
* 25,000 negative reviews

### Dataset Limitation

The IMDb dataset used in this project contains only positive and negative sentiment labels. It does not contain a neutral class. Therefore, this project performs binary sentiment classification rather than artificially creating neutral labels.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* Matplotlib
* WordCloud
* Jupyter Notebook

## Project Workflow

### 1. Data Loading

The IMDb dataset was loaded from the positive and negative review folders and combined into a single DataFrame.

### 2. Data Inspection

The dataset was inspected for:

* Number of rows and columns
* Missing values
* Duplicate reviews
* Sentiment distribution
* Sample reviews

### 3. Text Preprocessing

The following preprocessing steps were performed:

* Converted text to lowercase
* Removed HTML tags
* Removed punctuation
* Removed numbers
* Tokenised the text
* Removed English stopwords

### 4. TF-IDF Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert the cleaned text into numerical features that machine learning models can process.

The TF-IDF vectorizer was configured with up to 10,000 features and included unigrams and bigrams.

### 5. Train-Test Split

The dataset was divided into:

* 80% training data – 40,000 reviews
* 20% testing data – 10,000 reviews

### 6. Machine Learning Models

Two classifiers were trained:

* Multinomial Naive Bayes
* Logistic Regression

### 7. Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

### 8. Model Results

| Model               | Accuracy | F1-Score |
| ------------------- | -------: | -------: |
| Naive Bayes         |   86.75% |     0.87 |
| Logistic Regression |   89.57% |     0.90 |

Logistic Regression achieved the best performance with an accuracy of 89.57%.

### 9. Visualizations

The project includes:

* Sentiment distribution bar chart
* Naive Bayes confusion matrix
* Logistic Regression confusion matrix
* Model accuracy comparison chart
* Positive sentiment WordCloud
* Negative sentiment WordCloud

### 10. Error Analysis

Five misclassified reviews were examined to understand model errors.

The main causes identified were:

* Mixed sentiment
* Positive words appearing in negative reviews
* Sarcasm and irony
* Long and complex reviews
* Limited contextual understanding of TF-IDF

## Conclusion

The project successfully demonstrates a complete text sentiment classification pipeline using traditional machine learning techniques.

Among the two models, Logistic Regression performed better than Naive Bayes, achieving an accuracy of 89.57% and an F1-score of 0.90.

Sentiment analysis can be applied to customer feedback, movie reviews, social media monitoring, brand reputation analysis, and customer satisfaction analysis.

## Files

* `Sentiment_Analysis.ipynb` – Complete Jupyter Notebook
* `requirements.txt` – Required Python libraries
* `README.md` – Project documentation
