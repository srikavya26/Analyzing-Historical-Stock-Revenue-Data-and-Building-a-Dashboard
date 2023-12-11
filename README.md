## Analyzing Historical Stock/Revenue Data and Building a Dashboard
### https://www.coursera.org/learn/python-project-for-data-science?specialization=ibm-data-science
### https://jupyter.org/

### Description:
#### Extracting essential data from a dataset and displaying it is a necessary part of data science.
#### Using the yfinance Library to Extract Stock Data
The yfinance is a Python library that provides a user-friendly interface for downloading historical market data from Yahoo Finance. It allows you to get historical stock prices, dividends, and other financial data for stocks, Exchange-Traded Funds (ETFs), and other securities.

Using the Ticker module we can create an object that will allow us to access functions to extract data. To do this we need to provide the ticker symbol for the stock, here the company is Apple and the ticker symbol is AAPL.
```
import yfinance as yf

### Download historical data for a stock

msft = yf.Ticker("MSFT")
msft_data = msft.history(period="max")
### Display the downloaded data
msft_data.head()
```
#### Stock Info
Using the attribute info we can extract information about the stock as a Python dictionary.
#### Extracting Share Price
A share is the single smallest part of a company's stock that you can buy, the prices of these shares fluctuate over time. Using the history() method we can get the share price of the stock over a certain period of time. Using the period parameter we can set how far back from the present to get data. The options for period are 1 day (1d), 5d, 1 month (1mo) , 3mo, 6mo, 1 year (1y), 2y, 5y, 10y, ytd, and max.
#### Extracting Dividends
Dividends are the distribution of a companys profits to shareholders. In this case they are defined as an amount of money returned per share an investor owns. Using the variable `dividends` we can get a dataframe of the data. The period of the data is given by the period defined in the 'history` function.
<img width="1470" alt="Screenshot 2023-05-14 at 1 45 47 PM" src="https://github.com/srikavya26/Analyzing-Historical-Stock-Revenue-Data-and-Building-a-Dashboard/assets/95865936/63e55b4d-b38b-4a95-a265-c6d96b0470d9">
