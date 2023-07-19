# InvestmentStrategies

These are just some random investment strategy algorithms that I created a few years ago and I'm placing them here in case this can be of any help for you to perform some backtesting reasearch of some sort or anything you need for (do not recommend investing on this, even if strategies outperform, they are not adjusted to account for transaction costs).

For now this only has the Markoviwch Mean Variance Optimmization Strategy (Sharpe Ratio maximization), the Minimum variance portfolio, and the Equally weighted portfolio (1/N) with different rebalancing periods.

You give as input the matrix of prices in time-series, and the functions return the matrix of weights of the strategy also in time-series.

You have to provide the values in the same time frames. For example, if you provide a matrix of daily prices, then provide an approx for the risk-free rate also as a daily value (or just set it to 0 for simplification). The min periods and the variance window also have to be in the same time period as the price data. For example, in the sharpe ratio optimization strategy if the variance window is set to 20, then the algorithm will use the past 20 time series data information to compute the covariance matrix for it to maximize the sharpe ratio on that previous 20 periods.
