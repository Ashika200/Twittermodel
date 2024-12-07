# Twitter Sentiment Model
This project leverages real-time Twitter data to predict stock market trends based on sentiment analysis. By scraping tweets containing stock-related keywords, we preprocess the data to remove noise, then apply sentiment analysis using FinBERT to categorize the sentiment of each tweet as positive, negative, or neutral. The sentiment data, along with engagement metrics such as retweets and likes, are used to train a machine learning model (Random Forest) to predict stock price movements. The entire process is automated through Python scripts and Google Colab/Jupyter notebooks, with visualizations that provide insights into sentiment trends over time. The project is designed to help understand how public sentiment on social media platforms can potentially influence stock market behavior.

Here are the steps to run the project in Google Colab:

Install Dependencies:
!pip install tweepy transformers scikit-learn pandas plotly nltk

Set Up API Keys:
Create config.py in Colab with your Bearer Token from Twitter.

Run Twitter Scraper:
Use the provided Tweepy streaming code to scrape tweets based on keywords.

Preprocess Tweets:
Clean and tokenize the scraped tweets (remove URLs, mentions, etc.).

Sentiment Analysis:
Use FinBERT to perform sentiment analysis on tweets:
sentiment_pipeline = pipeline("sentiment-analysis", model="yiyanghkust/finbert-tone")

Train Prediction Model:
Use a RandomForestClassifier to predict stock trends based on sentiment and engagement metrics.

Visualize Sentiment Trends:
Plot sentiment trends over time using Plotly.

Export Data:
Save results (tweets, sentiment data, model outputs) using to_csv() or joblib.
These are the steps followed!
