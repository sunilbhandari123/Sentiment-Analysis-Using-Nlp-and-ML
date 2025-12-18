## Sentiment Analysis Using NLP
# Overview

This project implements an end-to-end sentiment analysis pipeline using Natural Language Processing (NLP) techniques. Tweets are classified into positive, neutral, and negative categories based on their textual content using multiple machine learning models.

# Dataset Description

The sentiment analysis dataset is automatically generated using emoticons as indicators of sentiment polarity. Tweets containing positive emoticons (e.g., :)) are labeled as positive, while tweets containing negative emoticons (e.g., :() are labeled as negative. Neutral tweets are also included.

The dataset is provided in CSV format and contains six fields:
1. Polarity – Sentiment label (0 = negative, 2 = neutral, 4 = positive)
2. Tweet ID – Unique identifier for each tweet
3. Tweet Date – Date and time of the tweet in UTC format
4. Query – Query term used in the tweet or NO_QUERY if none
5. Username – Twitter user who posted the tweet
6. Text – Tweet content with emoticons removed
This dataset is widely used by the data science community for sentiment analysis research and experimentation, allowing evaluation of different NLP techniques for emotion analysis.

## Project Workflow (Step-by-Step)

# 1. Import Libraries and Dataset
Required Python libraries and the sentiment dataset are imported to initialize the analysis environment.

# 2. Display Dataset
The dataset is displayed to understand its structure, columns, and sample records.

# 3. Display Maximum Rows and Columns
Display settings are adjusted to allow full visibility of dataset columns and records.

# 4. Check Data Types
Each column’s data type is examined to ensure correctness before preprocessing.

# 5. Convert to String Format
Text-based columns are converted to string format to avoid processing issues during NLP operations.

# 6. Remove Missing Values
Rows containing null or missing values are removed to maintain data quality.

# 7. Concatenate Dataset
If the dataset is split into multiple parts, they are combined into a single dataset for analysis.

# 8. Load Train and Test Dataset
The dataset is divided into training and testing sets for model evaluation.

# 9. Remove Unnecessary Characters
Special characters, URLs, punctuation, and symbols are removed from the text to reduce noise.

# 10. Convert Text to Lowercase
All text is converted to lowercase to ensure consistency during tokenization.

# 11. Remove Stopwords
Common stopwords that do not contribute to sentiment meaning are removed.

# 12. Tokenization
Text is split into individual tokens (words) for further linguistic processing.

# 13. Word Frequency Distribution
The frequency of words in the dataset is analyzed to identify common patterns.

# 14. Stemming Using Lancaster Stemmer
Words are reduced to their root forms using the Lancaster stemming algorithm.

# 15. Data Normalization
Processed text is normalized to prepare it for vectorization and modeling.

# 16. Sentiment Categorization
Sentiment labels are mapped to categorical values for classification tasks.

# 17. Sentiment Value Counts
The distribution of sentiment classes is analyzed to understand class balance.

# 18. Visualization Using Histplot
Data distributions and sentiment frequencies are visualized using histograms.

# 19. Create TF-IDF Features
Text data is transformed into numerical features using TF-IDF vectorization.

# 20. Apply Logistic Regression
A Logistic Regression model is trained on TF-IDF features to classify sentiment.

# 21. Apply Decision Tree Classifier
A Decision Tree model is trained to evaluate rule-based sentiment classification.

# 22. Apply Random Forest Classifier
A Random Forest model is trained to improve classification through ensemble learning.

# 23. Evaluation of Dataset
Models are evaluated using accuracy scores on the test dataset.


## Model Performance
# Model	Accuracy
Logistic Regression	82.86%
Random Forest Classifier	81.17%
Decision Tree Classifier	76.07%

Logistic Regression achieved the highest accuracy, followed by Random Forest and Decision Tree models.

## Conclusion

This project demonstrates how NLP preprocessing and feature extraction significantly influence sentiment classification performance. Among the evaluated models, Logistic Regression provided the best results, showing strong effectiveness for sentiment prediction on processed tweet data.

## Tools and Libraries

1. Python
2. NumPy
3. Pandas
4. NLTK
5. Scikit-learn
6. Matplotlib
7. Seaborn
