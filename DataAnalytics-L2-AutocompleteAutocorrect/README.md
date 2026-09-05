# Autocomplete and Autocorrect Data Analytics

## Project Overview

This project analyses the efficiency and accuracy of autocomplete and autocorrect techniques using Natural Language Processing (NLP). A text corpus from *Alice's Adventures in Wonderland* was used to build frequency-based n-gram models for autocomplete and an edit-distance-based spelling correction system for autocorrect.

The project compares Bigram and Trigram autocomplete approaches and evaluates their performance using accuracy, precision, and recall.

## Objective

* Analyse text data using NLP preprocessing techniques.
* Build a frequency-based Bigram autocomplete model.
* Build a frequency-based Trigram autocomplete model.
* Predict the next word for different prefixes.
* Implement autocorrect using `pyspellchecker`.
* Test autocorrect using 20 deliberately misspelled words.
* Calculate accuracy, precision, and recall.
* Compare Bigram and Trigram autocomplete performance.
* Visualize frequent words and autocorrect results.

## Dataset

The text corpus used in this project is *Alice's Adventures in Wonderland* by Lewis Carroll, obtained from Project Gutenberg.

The corpus is stored locally as:

`corpus.txt`

## Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Matplotlib
* Seaborn
* PySpellChecker
* Jupyter Notebook

## NLP Preprocessing

The following preprocessing steps were performed:

1. Converted the text to lowercase.
2. Tokenized the text into individual words.
3. Removed punctuation and non-alphabetic tokens.
4. Removed English stopwords for general NLP analysis.
5. Retained stopwords for autocomplete because words such as "the", "a", and "to" are important for predicting natural word sequences.

## Autocomplete

### Bigram Model

A Bigram model uses two consecutive words to learn which words commonly follow a given word.

For example, given a prefix such as:

`the`

the model returns the three most frequent next-word predictions.

The model was tested on 10 different prefixes.

### Trigram Model

A Trigram model uses two consecutive words to predict the next word.

For example:

`alice was → not, beginning, very`

The Trigram model was also evaluated using Top-3 prediction accuracy.

## Autocorrect

The `pyspellchecker` library was used to perform spelling correction based on edit distance and word frequency.

Twenty deliberately misspelled words were tested, including examples such as:

* `computr` → `computer`
* `frend` → `friend`
* `recieve` → `receive`
* `langauge` → `language`
* `analytcs` → `analytics`

## Performance Results

### Autocomplete

| Approach | Top-3 Accuracy | Precision | Recall |
| -------- | -------------: | --------: | -----: |
| Bigram   |         30.00% |      0.30 |   0.30 |
| Trigram  |         90.00% |      0.90 |   0.90 |

The Trigram model performed substantially better than the Bigram model because it uses more context when predicting the next word.

### Autocorrect

* Test cases: 20
* Correct predictions: 17
* Incorrect predictions: 3
* Accuracy: **85.00%**
* Precision: **0.85**
* Recall: **0.85**

## Visualizations

The project includes the following visualizations:

1. **Top 20 Most Frequent Words**

   * Shows the most frequently occurring words after NLP preprocessing.

2. **Bigram vs Trigram Autocomplete Performance**

   * Compares the Top-3 prediction accuracy of both approaches.

3. **Autocorrect Confusion Matrix**

   * Provides a simplified visualization of correct and incorrect autocorrect outcomes.

All visualization files are available in the `images` folder.

## Key Findings

* The Trigram model achieved **90% Top-3 accuracy**, compared with **30% for the Bigram model**.
* Using more contextual information significantly improved next-word prediction.
* The autocorrect system correctly predicted **17 out of 20** deliberately misspelled words.
* Frequency-based n-gram models are simple and interpretable but depend heavily on the words present in the training corpus.
* Edit-distance-based autocorrection works well for common spelling mistakes but may produce incorrect corrections for ambiguous words.

## Limitations

This project is an educational implementation and has several limitations:

* The corpus is relatively small compared with the datasets used by commercial keyboard applications.
* N-gram models cannot understand deeper semantic context.
* Words that are not present in the corpus may not receive useful autocomplete predictions.
* `pyspellchecker` may select an incorrect correction when multiple words are similarly close.
* The system does not learn individual user writing patterns.
* It does not consider keyboard layout errors, slang, emojis, abbreviations, or multilingual typing.
* The precision and recall calculations used in this project are simplified success-based evaluation metrics.
* The autocorrect confusion matrix is a simplified correct/incorrect outcome matrix rather than a conventional multi-class confusion matrix.

## Comparison with Modern Keyboard Systems

Applications such as Google Keyboard use much larger datasets and more advanced language models. Modern systems can consider sentence context, user-specific typing patterns, keyboard position, frequently used words, multilingual input, and continuously updated language models.

The models developed in this project demonstrate the basic principles behind autocomplete and autocorrect but are much simpler than production-level systems.

## Conclusion

This project demonstrates how NLP techniques can be used to implement basic autocomplete and autocorrect functionality.

The comparison shows that the **Trigram model performed better than the Bigram model**, achieving 90% Top-3 accuracy compared with 30%. This demonstrates the benefit of using additional context for next-word prediction.

The autocorrect system achieved **85% accuracy** on 20 deliberately misspelled words, showing that edit-distance-based spelling correction can effectively handle many common spelling errors.

For a more advanced system, larger text corpora, neural language models, contextual embeddings, user personalization, and keyboard-aware correction techniques could be incorporated.

## Project Structure

```text
DataAnalytics-L2-AutocompleteAutocorrect/
│
├── corpus.txt
├── Autocomplete_Autocorrect_Analysis.ipynb
├── README.md
├── requirements.txt
│
└── images/
    ├── top_20_words.png
    ├── autocomplete_comparison.png
    └── autocorrect_confusion_matrix.png
```

## How to Run

1. Install Python.
2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Open Jupyter Notebook:

```bash
jupyter notebook
```

4. Open the project notebook.
5. Run the cells from top to bottom.

## Author

**Sravya Masimukku**

**Data Analytics – OIBSIP Internship**
