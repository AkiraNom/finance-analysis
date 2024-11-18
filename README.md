# Stock and Index Beta Calculator #
Python script that calculates the beta (β) of a stock against the market index. The script retrieves the stock and index price data from yahoo finance. The beta is calculated by using both covariance/variance method and ordinary least square method.


## Background ##
The beta (β) of an investment security is a measurement of its volatility of returns relative to the entire market. It is used as a measure of risk and is an integral part of the Capital Asset Pricing Model (CAPM). A company with a higher beta has greater risk and also greater expected returns. <br>

<b>Major uses of beta</b>:
* Measuring the risk of a portfolio to the market
* Measuring the volatiltiy of an industry compared to the market
* Estimating the expected return on equity of stock in the Capital Asset Pricing Model (CAPM)

## Process ##
There are two methods used to compute beta.
1. Using the formala, $$\beta = Cov(r_i, r_m)/Var(r_m)$$ The covariance between the returns of a security and returns of the market divided by the volatility of the market.
2. Plot a scatter plot of the returns of the market against the returns of a securit. The slope of the best fitted trendline is the extimated beta.

In theory, both betas should be the same.

## Usage ##
This is an interactive web application developed with streamlit. [Streamlit app](https://finance-analysis-j22zwkeeepzxpym9ej9smg.streamlit.app/)

1. Type any ticker available on the yahoo finance. The default is 'AAPL'.
2. Select market index among US three major indices. Currently, only US indices are listed. It may be expanded in future.

    Country | Major Index | Name
    | :--- | :--: |:--:
    United States | ^SPX  |S&P500
    United States | ^IXIC | Nasdaq
    United States | ^DJI  | Dow Jones

3. Select date range (start, end), and data interval (weekly or monthly)

4. Betas are computed and adjusted betas are also provided. (Blume adjuetment)
## Required Libraries ##
* numpy
* pandas
* plotly
* streamlit
* statsmodels
* yfinance
