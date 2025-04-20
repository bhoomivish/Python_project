## Portfolio-Based Stock Allocator using yFinance in Python

Overview

This project provides a smart, data-driven solution to help investors determine how many shares of top-performing companies they can purchase based on their portfolio size. By leveraging live financial data from Yahoo Finance, it identifies the top 10 companies by market capitalization and calculates the number of shares one can buy in each, making investing efficient and transparent.

Business Problem

The goal is to simplify the investment decision-making process for retail investors by:
•	Identifying the top companies based on market capitalization.
•	Allowing users to input their total investable portfolio size.
•	Automatically computing the number of shares to buy for each selected stock.
This tool can assist both beginners and seasoned investors in allocating their funds more efficiently.

Dataset

The project uses a CSV file (top 50 stock.csv) containing ticker symbols of the top 50 NSE-listed companies. These symbols are used to fetch live market data via the Yahoo Finance API.
Sample Columns:
•	Ticker: NSE ticker symbol of the company.

Key Features

The code performs the following:
•	Downloads market data (price and market cap) for listed tickers using yfinance.
•	Sorts companies by market capitalization in descending order.
•	Selects the top 10 companies.
•	Accepts portfolio size as user input.
•	Calculates equal allocation per stock.
•	Computes how many shares of each stock can be bought.

Tools and Technologies

•	Language: Python 3
•	Libraries:
	pandas (data manipulation)
	numpy (numerical operations)
	yfinance (fetching financial data)
	math (floor function for integer share calculation)

Methodology
1. Data Collection
   
•	Read tickers from a CSV file.
•	Fetch live stock data (Close price, Market Cap) using yfinance.

3. Data Processing
•	Sort stocks by market cap.
•	Slice the top 10 stocks.
•	Reset the index for clean presentation.

5. Share Calculation Logic
•	Input portfolio size from the user.
•	Divide portfolio equally among 10 companies.
•	Calculate number of shares = Floor(Position Size / Latest Stock Price)

Conclusion

This project is a practical example of combining finance and programming to build personalized investment tools. It simplifies investment allocation and demonstrates:
•	Data-driven decision making.
•	Real-time financial data analysis.
•	Python's ability to solve real-world finance problems efficiently.
