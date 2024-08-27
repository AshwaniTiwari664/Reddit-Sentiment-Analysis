# Reddit Sentiment Analysis

## Overview
This program analyzes Reddit posts to identify the most frequently mentioned stock tickers and evaluates their sentiment using Vader SentimentIntensityAnalyzer. It helps to gauge public sentiment and trends around specific stocks by analyzing user comments and post data.

## Program Parameters
- **`subs`**: List of subreddits to search.
- **`post_flairs`**: Dictionary of post flairs to filter posts. Posts with `None` flair are automatically included.
- **`goodAuth`**: Dictionary of authors allowed more than one comment per symbol.
- **`uniqueCmt`**: Boolean to allow only one comment per author per symbol.
- **`ignoreAuthP`**: Dictionary of authors to ignore for posts.
- **`ignoreAuthC`**: Dictionary of authors to ignore for comments.
- **`upvoteRatio`**: Minimum upvote ratio for posts to be considered (e.g., `0.70` for 70%).
- **`ups`**: Minimum number of upvotes for posts to be considered.
- **`limit`**: Limit for the number of comments to analyze.
- **`upvotes`**: Minimum number of upvotes for comments to be considered.
- **`picks`**: Number of top mentions to display.
- **`picks_ayz`**: Number of top picks to include in sentiment analysis.

## How to Run
1. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2. Run the analysis script:
    ```bash
    python reddit-sentiment-analysis.py
    ```

## Sample Output
![image](https://github.com/user-attachments/assets/d7005b01-108c-49ba-99e2-bb2df1c67e76)

It took 1574.61 seconds to analyze 14236 comments in 8 posts in 1 subreddit.


**10 Most Mentioned Picks:**
- GME: 764
- SPCE: 183
- PLTR: 89
- TSLA: 71
- MVIS: 42
- NVDA: 34
- AMD: 30
- F: 29
- TLRY: 29
- AAPL: 26

**Sentiment Analysis of Top 5 Picks:**

| Ticker | Bearish | Neutral | Bullish | Total/Compound |
|--------|---------|---------|---------|----------------|
| GME    | 0.087   | 0.707   | 1.548   | 0.030          |
| SPCE   | 0.119   | 0.645   | 1.618   | 0.027          |
| PLTR   | 0.073   | 0.649   | 1.751   | 0.032          |
| TSLA   | 0.088   | 0.650   | 1.543   | 0.049          |
| MVIS   | 0.155   | 0.698   | 1.714   | -0.020         |

## Data
The analysis includes US stocks with a market cap greater than $100 million and a price above $3, excluding penny stocks. You can download stock data from the following source:
- [US Stocks Data](https://www.nasdaq.com/market-activity/stocks/screener?exchange=nasdaq&letter=0&render=download)

## License
This project is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for details.
