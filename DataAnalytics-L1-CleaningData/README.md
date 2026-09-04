# OASIS INFOBYTE – Data Analytics Internship

## Task 3 – Cleaning Data

### Objective

The objective of this task is to demonstrate professional data cleaning skills by transforming a deliberately messy dataset into a clean and analysis-ready dataset using Python, pandas, and NumPy.

### Dataset

The dataset contains information about the highest-grossing music tours by women. The original dataset was obtained from Kaggle and contained missing values, inconsistent formatting, citation markers, currency symbols, and unnecessary reference information.

### Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook

### Data Cleaning Steps

The following cleaning operations were performed:

1. **Data Quality Assessment**

   * Checked dataset dimensions.
   * Examined data types.
   * Identified missing values.
   * Checked duplicate records.
   * Inspected unique values and potential anomalies.

2. **Missing Data Handling**

   * Missing values were identified in the `Peak` and `All Time Peak` columns.
   * Since unavailable ranking information could not be reliably inferred, these values were represented as `Unknown`.
   * No rows were deleted.

3. **Duplicate Removal**

   * Duplicate records were checked.
   * No duplicate rows were found.

4. **Standardisation**

   * Citation markers were removed from ranking values.
   * Currency symbols, commas, and citation characters were removed from monetary values.
   * Unwanted symbols and citation markers were removed from tour titles.
   * The `Year(s)` column was standardized by replacing en dashes with hyphens.

5. **Data Type Correction**

   * Monetary columns were converted to floating-point values.
   * `Rank` and `Shows` were retained as integers.
   * Ranking columns were kept as strings to preserve the `Unknown` category.
   * A `Start Year` numerical column was created from the first year of each tour.

6. **Outlier Detection**

   * The Interquartile Range (IQR) method was used to identify potential outliers.
   * The identified values were reviewed and found to represent genuine observations rather than data errors.
   * Therefore, the outliers were retained.

7. **Unnecessary Column Removal**

   * The `Ref.` column was removed because it contained source citation information that was not required for analysis.

### Before vs After Cleaning

| Metric          |  Before Cleaning | After Cleaning |
| --------------- | ---------------: | -------------: |
| Null Count      |               25 |              0 |
| Duplicate Count |                0 |              0 |
| Row Count       |               20 |             20 |
| Dtype Accuracy  | Needs correction |        Correct |

### Final Dataset

The final cleaned dataset contains:

* **20 rows**
* **10 columns**
* **0 missing values**
* **0 duplicate rows**

The cleaned dataset is saved as:

`cleaned_music_tours.csv`

### Files Included

* `Data_Cleaning_Analysis.ipynb` – Jupyter Notebook containing the complete cleaning process and explanations.
* `dirty_music_tours.csv` – Original messy dataset.
* `cleaned_music_tours.csv` – Final cleaned dataset.
* `README.md` – Project documentation.

### Conclusion

The messy music-tour dataset was successfully transformed into an analysis-ready dataset. Missing values, duplicate records, inconsistent formatting, unwanted symbols, incorrect data types, and potential outliers were systematically investigated and handled. All cleaning decisions were documented to ensure transparency and reproducibility.
