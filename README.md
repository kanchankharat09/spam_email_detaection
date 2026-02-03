SMS Spam Detection Project
This project is a Machine Learning-based SMS Spam Classifier that identifies whether a text message is Ham (legitimate) or Spam. It features a full pipeline from raw data cleaning to model deployment readiness.

Project Overview
The goal was to build a highly precise model. In spam detection, Precision is more important than Accuracy because we want to avoid "False Positives" (marking a real message as spam).

1. Data Cleaning
Removed unnecessary columns and handled null values.
Encoded labels: 0 for Ham and 1 for Spam.
Removed duplicate entries to prevent model bias.

2 Exploratory Data Analysis (EDA)
Analyzed the distribution of characters, words, and sentences using nltk.
Insight: Spam messages tend to have a higher number of characters and words compared to ham messages.
Visualized data using Pie charts, Histograms, and Heatmaps.

3. Text Preprocessing
A custom transform_text function was built to:
Convert text to Lowercase.
Tokenize sentences into individual words.
Remove Special Characters and Punctuation.

Filter out Stopwords (common words like "the", "is", etc.).

Apply Stemming (e.g., "loving" → "love") using the PorterStemmer.



4. Model Building & Evaluation
We tested three variants of Naive Bayes using both CountVectorizer and TfidfVectorizer:
GaussianNB
MultinomialNB
BernoulliNB
The Winner: TfidfVectorizer + MultinomialNB
Accuracy: ~97%
Precision: 1.0 (100%) — This ensures no legitimate messages are incorrectly flagged as spam.

 Tech Stack
Language: Python
Libraries: Pandas, NumPy, Scikit-learn, NLTK, Seaborn, Matplotlib

Tools: WordCloud (for keyword visualization), Pickle (for model export)

Files for Deployment
vectorizer.pkl: The saved TF-IDF vectorizer.
model.pkl: The trained Multinomial Naive Bayes model.
