# Stock Sentiment Analysis Using Machine Learning Techniques

## Project Overview

This project aims to develop a sentiment analysis model to predict stock price movements based on textual data from news articles, social media posts, and other financial sources. By analyzing sentiment in text, the model provides insights into investor and market sentiment to inform trading decisions.

## Data Collection

### Async PRAW (Reddit API)

- **Purpose:** Fetching posts from the Facebook subreddit for sentiment analysis.
- **Implementation:** Utilized Async PRAW, a Python wrapper for the Reddit API.
  - Initialized Async PRAW with appropriate Reddit API credentials.
  - Accessed the Facebook subreddit and fetched posts using asynchronous methods.
  - Stored data in a Pandas DataFrame with relevant attributes.

### Yahoo Finance API

- **Purpose:** Retrieving historical stock data for the "META" symbol.
- **Implementation:** Used the Yahoo Finance API to download and analyze historical stock data.
  - Imported the `yfinance` library and specified the stock symbol and date range.
  - Downloaded daily stock price data into a Pandas DataFrame.
  - Calculated daily returns and assigned labels ('increase', 'decrease', 'no_change').

## Data Preprocessing

- **Textual Data Cleaning:**
  - Cleansed textual data to remove noise and standardize text representations.
  - Implemented functions for cleaning, removing URLs, lowercase conversion, stopword removal, and lemmatization using NLTK.

## Sentiment Analysis

- **Sentiment Scoring:**
  - Used `SentimentIntensityAnalyzer` from NLTK's VADER module for sentiment scores.
  - Employed `TextBlob` for sentiment label classification (positive, negative, neutral).
  - Extracted sentiment polarity and subjectivity scores for analysis.

## Stock Price Analysis

- **Analysis of Historical Stock Data:**
  - Analyzed daily returns and stock price movements for "META" stock.
  - Prepared datasets for model training by merging sentiment analysis results with stock price data.

## Machine Learning Models

- **Model Training and Evaluation:**
  - Trained classification models (Logistic Regression, SVM, Random Forest, KNN) using TF-IDF vectorization.
  - Evaluated model performance with metrics like accuracy, precision, recall, and F1-score.
  - Conducted error handling and exception management during model training.

## Strategy Evaluation

- **Sentiment-Based Trading Strategy:**
  - Developed a trading strategy using sentiment scores to determine buy and sell signals.
  - Calculated cumulative returns and Sharpe ratio to assess strategy performance.
  - Visualized performance metrics (cumulative returns, Sharpe ratio).

## Results and Discussion

- **Model Performance:**
  - Evaluated sentiment-based trading strategy against buy-and-hold strategy.
  - Analyzed risk factors including maximum drawdowns and trade win ratio.
- **Conclusion:**
  - Successfully developed a sentiment analysis model for stock price prediction.
  - Highlighted the value of sentiment analysis in enhancing trading decisions.
  - Proposed future work to improve model robustness and predictive accuracy.

