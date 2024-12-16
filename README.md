# Portfolio Optimization

## Description

This project performs stock portfolio optimization by analyzing stock prices of selected companies over several years. The goal is to simulate portfolios based on various risk levels, calculate their returns and volatility, and recommend the best portfolio based on the user’s desired risk.

The project uses the Yahoo Finance API to fetch stock data for multiple years and computes correlation, covariance, variance, and standard deviation for selected stocks. It then simulates different portfolios, calculating their returns and volatility, and recommends the portfolio with the highest return for a given risk level.

## Features

- Fetch stock prices for selected symbols from Yahoo Finance.
- Calculate the correlation matrix, covariance matrix, variance, and standard deviation for each stock.
- Simulate multiple portfolios with different weightings of stocks and calculate their returns and volatility.
- Recommend the portfolio with the highest return for a user-specified risk level.
- Visualize the simulated portfolios with a scatter plot showing volatility versus return.

## Requirements

- Python 3.x
- yfinance library
- pandas library
- numpy library
- matplotlib (for plotting)


## Usage

1. Run the script to fetch stock prices and calculate the correlation and covariance matrices for each year.
2. Simulate multiple portfolios and display the results in a scatter plot, showing the relationship between volatility and return.
3. Enter your desired risk level (in percentage) when prompted to receive the optimal portfolio with the highest return for that risk level.


## Functions

- `fetch_stock_prices(start_date, end_date, symbols)`: Fetches adjusted closing stock prices from Yahoo Finance for the specified symbols and date range.
- `calculate_correlation(prices)`: Calculates the correlation matrix for the given stock prices.
- `calculate_covariance_matrix(prices)`: Calculates the covariance matrix for the given stock prices.
- `find_closest_to_zero_correlation(prices)`: Finds the pair of stocks with the correlation closest to zero.
- `calculate_variance(portfolio_prices)`: Calculates the variance of returns for the given portfolio of stocks.
- `calculate_std_dev(variance)`: Calculates the standard deviation of returns for the given portfolio of stocks.
- `get_highest_return_asset(portfolios, target_risk, tolerance)`: Finds the portfolio with the highest return for a given risk level.

## Example Output

When you run the script, you will see the following:

1. Correlation and covariance matrices for each year.
2. A scatter plot visualizing the simulated portfolios with their respective returns and volatility.
3. The optimal portfolio for the specified risk level, including the weights of each stock in the portfolio.

### Example input and output:

```
Enter your desired risk level (in percentage): 10
For a risk level of 10.0%, the portfolio with the highest return is:
Returns         0.14
Volatility      0.08
AAPL_Weight     0.56
TSLA_Weight     0.44
Name: 785, dtype: float64
```

## Technologies Used

- **Python 3.x**: Programming language used for the implementation.
- **yfinance**: Library for fetching stock data from Yahoo Finance.
- **pandas**: Library for handling and analyzing data.
- **numpy**: Library for numerical operations.
- **matplotlib**: Library for creating visualizations.
