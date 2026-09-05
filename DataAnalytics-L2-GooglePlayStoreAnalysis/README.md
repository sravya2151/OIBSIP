# Google Play Store Analysis

## Project Overview

This project analyzes the Google Play Store ecosystem to identify patterns in app categories, ratings, installs, pricing, estimated revenue, and user review sentiment.

The analysis includes data cleaning, exploratory data analysis, visualization, sentiment analysis, and business recommendations for app developers.

## Objectives

* Clean and prepare Google Play Store app data.
* Analyze app distribution across categories.
* Study app rating patterns.
* Investigate the relationship between app size and installs.
* Compare free and paid applications.
* Analyze paid app pricing.
* Estimate revenue by app category.
* Analyze user review sentiment.
* Identify positive and less-positive sentiment across categories.
* Provide data-driven recommendations for app developers.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* TextBlob
* Plotly
* Jupyter Notebook

## Datasets

The project uses two datasets:

1. Google Play Store Apps dataset
2. Google Play Store User Reviews dataset

The app dataset contains information such as category, ratings, installs, pricing, app size, and other application attributes.

The user reviews dataset contains review text and sentiment-related information.

## Data Cleaning

The following preprocessing steps were performed:

* Removed duplicate records.
* Converted `Installs` values into numeric format.
* Converted `Price` values into numeric format.
* Converted app sizes into MB.
* Converted ratings into numeric format.
* Handled missing values.
* Removed user reviews with missing review text.
* Cleaned review text by removing unnecessary spaces and converting text to lowercase.
* Generated sentiment polarity using TextBlob.

## Analysis Performed

### App Categories

The distribution of applications across Google Play Store categories was analyzed to identify highly populated and potentially saturated categories.

### Ratings

App rating distributions and average ratings by category were analyzed.

### Size vs Installs

A scatter plot was used to investigate the relationship between application size and number of installs.

The calculated correlation was approximately **0.0063**, indicating almost no linear relationship.

### Pricing

Free and paid applications were compared. Approximately **98.05%** of applications were free, while **1.95%** were paid.

The paid app price distribution was also analyzed.

### Estimated Revenue

Estimated revenue was calculated using:

`Price × Installs`

This provides an approximate revenue measure and should not be interpreted as actual reported revenue.

### Sentiment Analysis

User reviews were analyzed using TextBlob to classify reviews into:

* Positive
* Neutral
* Negative

Sentiment was also analyzed across app categories.

## Key Findings

* **Education** was the largest category, with approximately **241,090 apps**.
* The Google Play Store dataset is strongly dominated by free applications.
* The median price of paid applications was approximately **$1.99**.
* App size showed almost no linear relationship with installs.
* **Arcade** had the highest estimated revenue among paid-app categories in this analysis.
* **Role Playing** had the highest average app rating among categories.
* **Events** had the lowest average app rating.
* User review sentiment was generally positive across the analyzed categories.

## Business Recommendations

1. Developers should differentiate their products when entering highly saturated categories such as Education.
2. Free or freemium monetization strategies should be considered because free applications dominate the dataset.
3. Developers should prioritize user experience, application quality, and useful features rather than relying on application size to increase installs.
4. User reviews and sentiment should be monitored regularly to identify areas for product improvement.
5. Categories with strong estimated revenue potential can be investigated for monetization opportunities.

## Project Structure

```text
DataAnalytics-L2-GooglePlayStoreAnalysis/
│
├── Google-Playstore.csv
├── Google-Playstore-Cleaned.csv
├── googleplaystore_user_reviews.csv
├── googleplaystore_user_reviews_Cleaned.csv
├── Google_Play_Store_Analysis.ipynb
├── README.md
│
└── images/
    ├── category_distribution.png
    ├── rating_distribution.png
    ├── average_rating_by_category.png
    ├── size_vs_installs.png
    ├── free_vs_paid.png
    ├── paid_price_distribution.png
    ├── revenue_by_category.png
    ├── sentiment_distribution.png
    ├── sentiment_polarity_distribution.png
    ├── sentiment_by_category.png
    └── interactive_category_distribution.html
```

## Conclusion

The analysis demonstrates how app category competition, ratings, installs, pricing, estimated revenue, and user sentiment can be combined to understand the Google Play Store ecosystem.

These insights can help developers identify market opportunities, improve application quality, and make more informed decisions about positioning and monetization.
