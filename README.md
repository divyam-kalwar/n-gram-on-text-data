Sentiment Analysis on News Headlines - GitHub Repository README

Introduction
This GitHub repository contains code for performing sentiment analysis on a dataset of news headlines. The analysis includes data preprocessing, feature extraction, and n-gram analysis to gain insights into the most frequently occurring words and phrases in different sentiment categories.

Dataset
The dataset used for this analysis is sourced from Kaggle and includes news headlines labeled with sentiments (Neutral, Positive, Negative). It contains 4846 rows and two columns: 'Sentiment' and 'News Headline.' The data has been preprocessed, and no missing values are present.

Code Structure
File Upload and Kaggle API Setup:

The initial step involves uploading the dataset file to the Colab environment and configuring the Kaggle API for data download.
Data Download and Unzipping:

The Kaggle dataset is downloaded using the Kaggle API command, and the files are unzipped for further use.
Exploratory Data Analysis (EDA):

Information about the dataset is displayed using df.info().
The number of null values in the dataset is checked using df.isna().sum().
The distribution of sentiments is analyzed with df['Sentiment'].value_counts().
Feature Extraction:

The 'News Headline' column is extracted as the feature ('x') and the 'Sentiment' column as the target variable ('y').
Train-Test Split:

The data is split into training and testing sets using train_test_split() from scikit-learn. A 60-40 ratio is chosen for better insights.
Creating DataFrames:

Two DataFrames, df_train and df_test, are created to store the training and testing data, respectively.
Basic Pre-Processing:

Punctuation is removed from the 'News Headline' column in both the training and testing DataFrames.
Stopwords are removed using the NLTK library.
N-gram Analysis:

Custom functions are created to generate unigrams, bigrams, and trigrams.
The most frequently occurring words and phrases are visualized for each sentiment category.
Results
Unigram Analysis:

Top 10 words for Positive, Negative, and Neutral sentiments are visualized.
Bigram Analysis:

Top 10 bigrams for Positive, Negative, and Neutral sentiments are visualized.
Trigram Analysis:

Top 10 trigrams for Positive, Negative, and Neutral sentiments are visualized.
Conclusion
This repository provides a comprehensive analysis of sentiment in news headlines. The visualizations of the most common words and phrases for each sentiment category offer insights into the language patterns associated with different sentiments. Researchers and practitioners in natural language processing and sentiment analysis can benefit from this exploratory analysis.
