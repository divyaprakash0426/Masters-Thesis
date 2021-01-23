# Long Short Equity Strategy Using Sentiment
Automated trading systems or algorithmic trading is a method of
executing trade orders using automated pre-programmed trading instructions accounting
for variables such as time, price of stocks, and volume. The aim of the algorithmic trading
program is to dynamically identify profitable opportunities and place the trades in order to
generate profits at a speed and frequency that is impossible to match by
human traders.

### Quantopian's Research Environment
Any trading strategy requires a set of calculations on multiple data inputs to analyze large
amounts of assets at a time. The study deals with calculations that include selecting assets
based on filtering rules, ranking assets based on a scoring function, calculating sentiment
score for the underlying assets, trading strategy development and analysis and backtesting
on historical data.  
These calculations converge into an efficient Long-Short Equity trading
strategy. The performance of the algorithm is evaluated using statistical methods involving
returns plots, market beta, rolling plots and risk analysis. 

### Finding Patterns in Daily Returns and Public Sentiment
When exploring a dataset, we try to look for patterns that might serve as the basis for a
trading strategy. The plot shown is figure below uses PsychSignal's Trader Mood dataset for
Apple stocks which assigns bull and bear scores to stocks each day based on the aggregate
public sentiment from messages posted on Stocktwits, a financial communications
platform. The [notebook](https://github.com/divyaprakash0426/Quantopian-Long-Short-Equity-Strategy/blob/master/sentiment_intuition/SMA_tesla%20and%20apple.ipynb) explaining the same can be viewed in the repo.  
![Plot of daily returns, message volume and sentiment score of Apple stocks.](https://github.com/divyaprakash0426/Quantopian-Long-Short-Equity-Strategy/blob/master/images/sentiment_intuition.png)

### Ranking Schema and Alpha
The ranking schema considerers assets with a high 3 day average sentiment score as high
value, and assets with a low 3 day average sentiment score as low value.  
The algorithm uses Quantopian's open source factor analysis tool, Alphalens, to
test the quality of the selection strategy. Alpha factors express a predictive relationship
between some given set of information and future returns. By applying this relationship to
multiple stocks we can hope to generate an alpha signal and trade off of it. Refer to this [notebook](https://github.com/divyaprakash0426/Quantopian-Long-Short-Equity-Strategy/blob/master/strategy_development/long_short.ipynb) for detailed analysis.  

### Results
Backtesting simulation involves testing a trading strategy on historical data. It estimates
the strategy’s practicality and profitability on past data, validating it for success or failure
or any needed changes. The simulation is performed on the porfolio data for the time period
starting from January 2017 to December 2109 with an initial investment of 1 million
dollars.   
Algorithm performance over benchmark index SPY ![](https://github.com/divyaprakash0426/Quantopian-Long-Short-Equity-Strategy/blob/master/images/algo_performance.png)

Refer to [report](https://github.com/divyaprakash0426/Quantopian-Long-Short-Equity-Strategy/blob/master/report/report.pdf) for further details on backtest analysis, cumulative returns and risk exposure summary.

