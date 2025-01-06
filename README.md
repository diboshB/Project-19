# Project-19
NLP API - Stock market news - Apple Inc


1. Introduction
Sentiment analysis is the process of determining whether a piece
of text expresses positive, negative, or neutral sentiment. In the
context of financial markets, sentiment analysis on news articles
related to companies can provide valuable insights into how news
events impact stock prices and investor perceptions. This project
aims to analyze news headlines and summaries related to Apple
Inc. (AAPL) using sentiment analysis, and explore how the
sentiment may correlate with stock market movements. The goal
is to apply Natural Language Processing (NLP) techniques to
assess the polarity (positive or negative sentiment) of news
content and investigate whether sentiment influences stock price
changes.
The project uses the Finnhub API to fetch news data for Apple
Inc. and the TextBlob library for sentiment analysis. By applying
NLP techniques, this project attempts to understand the
sentiment expressed in news headlines and summaries and
analyze its potential impact on the stock market price of Apple.
2. Data Collection
The data for this project is collected through the Finnhub API,
which provides access to real-time news data related to various
companies. Specifically, the news articles related to Apple Inc.
(AAPL) were fetched using the company_newsfunction from the
Finnhub API. The data consists of the following attributes:
• Headline: The title of the news article.
• Summary: A brief description or summary of the article.
• Datetime: The publication date and time of the news
article.
• Source: The news outlet or website from which the article
originates.
The data collected covers a time range from January 1, 2024,
to January 31, 2024, allowing for a focused analysis of
sentiment over a one-month period.
3. Data Preprocessing
Several preprocessing steps were applied to the news data to
make it ready for sentiment analysis:
3.1 Handling Missing Values
The dataset was checked for missing values, particularly in the
"headline" and "summary" columns. Any rows with missing values
were removed to ensure a clean dataset for analysis.
3.2 Text Cleaning
The news headlines and summaries were cleaned by removing
any irrelevant characters such as special symbols, extra spaces,
and stop words. This step ensures that the text is standardized
and ready for sentiment analysis.
3.3 Sentiment Analysis
The main feature of this project is performing sentiment analysis
on the text data. The TextBlob library was used to calculate
the polarity score of the headlines and summaries. The polarity
score ranges from -1 (negative sentiment) to +1 (positive
sentiment), with values close to 0 indicating neutral sentiment.
The sentiment analysis is applied as follows:
• Headline Sentiment: Sentiment score calculated for the
headline of each news article.
• Summary Sentiment: Sentiment score calculated for the
summary of each news article.
4. Model Building
The goal of this project is to investigate the relationship between
sentiment and stock market movements. To achieve this, the
following steps were taken:
4.1 Stock Price Data Collection
Alongside the news data, Apple Inc.'s stock price data (AAPL) was
also fetched using the Finnhub API. The stock data includes:
• Date: The date on which the stock data was recorded.
• Open: The opening price of AAPL stock on that date.
• Close: The closing price of AAPL stock on that date.
• High: The highest price of AAPL stock on that date.
• Low: The lowest price of AAPL stock on that date.
• Volume: The trading volume of AAPL stock on that date.
The stock price data was aligned with the news data based on the
publication date and time.
4.2 Sentiment-Stock Price Relationship
Once sentiment scores were calculated for each news headline
and summary, the next step was to analyze whether sentiment
correlated with stock price movements. For this, the following
steps were followed:
• Calculate the average sentiment for news headlines and
summaries on a daily basis.
• Compare sentiment scores with the daily closing price of
AAPL.
• Investigate any patterns or correlations between sentiment
and price fluctuations.
4.3 Data Visualization
Various plots were created to visualize the relationship between
sentiment and stock prices. Key visualizations include:
• Sentiment over time: A line plot showing the daily
sentiment scores for headlines and summaries.
• Stock price over time: A line plot showing the daily closing
price of AAPL.
• Sentiment vs. Stock Price: Scatter plots to analyze if a
strong correlation exists between sentiment scores and
stock price changes.
5. Model Evaluation
5.1 Sentiment Analysis Evaluation
The effectiveness of sentiment analysis was evaluated by:
• Accuracy of Sentiment Classification: Checking if the
polarity values correctly capture the overall tone of the news
articles (positive, negative, or neutral).
• Correlation with Stock Price Movements: Analyzing the
correlation between sentiment scores and stock price
changes to determine if sentiment provides useful insights
into market behavior.
5.2 Evaluation Metrics
Since this project is focused on exploratory data analysis rather
than prediction, there are no formal metrics like accuracy,
precision, or recall. Instead, the evaluation focused on:
• Sentiment Score Distribution: The distribution of
sentiment scores for the headlines and summaries.
• Correlation: Pearson correlation coefficient between
sentiment and stock price movements.
6. Results & Discussion
6.1 Sentiment Analysis Results
The sentiment analysis revealed that the headlines for Apple Inc.
during January 2024 tended to be relatively neutral, with most
sentiment scores falling between -0.2 and +0.2. However, certain
spikes in positive or negative sentiment were observed, often
linked to major news events (e.g., product launches, earnings
reports, or regulatory news).
6.2 Sentiment and Stock Price Relationship
The analysis of sentiment against stock price changes showed:
• A weak positive correlation between headline sentiment
and stock price movements. This suggests that positive
news headlines may have a slight tendency to correlate with
stock price increases.
• The summary sentiment exhibited a slightly stronger
correlation with stock price, particularly when the sentiment
was extremely positive or negative.
6.3 Limitations
While sentiment analysis provides interesting insights, the
relationship between sentiment and stock price is not
straightforward. Stock prices are influenced by various factors,
such as market conditions, broader economic news, and investor
behavior, which are not always captured by sentiment alone.
7. Conclusion
This project successfully demonstrated the use of sentiment
analysis to analyze news related to Apple Inc. (AAPL) and its
potential impact on stock price movements. The sentiment
analysis revealed a general neutrality in the news, with occasional
spikes in positive or negative sentiment. The correlation analysis
between sentiment and stock price changes showed a weak
positive relationship, suggesting that sentiment may have some
impact on stock market behavior, but it is not the sole
determining factor.
