# Interactive Crypto Portfolio Analyzer
---

# Overview
The Interactive Crypto Portfolio Analyzer and Arbitrage Dectection App is used to determine the volitilaty and identify instances of arbitrage within the crypto exchanges.

The Apps main functionalities include:
- Use an interactive web GUI
- Analyze the risk indicators  of crypto currencies 
- Multiple crypto currencies are traded on several crypto exchanges
- Uncover patterns in the crypto market price data
- Detect arbitrage opportunities

- The app will analyze the risk indicators  of several crypto currencies traded on several crypto exchanges to uncover patterns in the crypto market. To do so the following tasks are performed: 
	- Calculate the daily returns of a stock traded on seevral exchanges
	- Analyze the volatility of each of the stocks listed on in the desired ETF
	- Evaluate the risk profile of each stock by using the standard deviation and the beta
	- Calculate the Sharpe ratios for each portfolio to determine the risk-retun profile.

# Functionalities supported	
- It offers an interactive web GUI to allow the user to select:

	- The choice of risk indicator (standard deviation, beta, daily returns and sharpe ratio) based on an 180 days rolling window
	- The choice of one ten crypto currency to analyse
		BTC - Bitcoin
		XRP - XRP Ledger
		ETH - Ether
		BCH - Bitcoin Cash
		LTC - Litecoin
		EOS - EOS
		XMR - Monero
		XLM - Stellar Lumens 
		ADA - Cardano
		XTZ - Tezos
		
	- The crypto currency closing value are compared on five crypto exchanges: Coinbase,Bittrex,Bitstamp,Kraken,Gemini
        - The choice of rolling windwo size (1, 7 , 30, or 180 days)

# Data Collection and Preparation
- Source data file: historical single crypto csv file
- 10 crypto currencies, 5 crypto exchanges, hourly price from 7/23/2013 to 7/31/2019
- Use pandas to build an on-demand dataframe
- DF includes only the daily closing prices for each crypto currency on all the five exchanges


# Directory structure
## app.py - main module
    - Build an interactive web GUI with dropdown menu
    - Call the processing module and plot the resulting graph
    - Allow user to  interact with the graph using a toolbar - Provide tooltips for additional description of  
      the axes and data of the graph

## data directory
    - crypto.csv

## Utils subdirectory
    - data_prep.py : clean up and prepare on demand dataframe based on user input cryptocurrency
    - sharpe_ratio.py : rolling window sharpe with selectable window size and selectable crypto currency
    - daily_returns.py : rolling window daily returns with selectable window size and selectable crypto
       currency
    - arbitrage.py :  rolling window closing prices of selectable crypto currency on exchanges


# Installation Guide
---
	The following packages are required:
		dash
		plotly
		pandas
		dash_bootstrap_components
		plotly.express
		numpy
		python3
		pathlib
	To install clone the repo and install the required packages
	- To run type the following  comand line: 'py app.py'
		
# Usage
---
 ## To run the app:
	- Open a command line and type: python app.py
	- The result on the command line:
		$ py app.py
			Dash is running on http://127.0.0.1:8050/

			* Serving Flask app 'app'
			* Debug mode: on
            Open a browser and connect to http://127.0.0.1:8050/
	
		- Select one of 4 risk indicator
		- Select of 10 cryptocurrencies
		- Select one of 4 rolling wndow sizes
		- The graph will be updated with the selected options
![image](https://github.com/Bakoroba/interactive_crypto_portfolio_analyzer/assets/7796158/e8e0d926-98e3-4980-b7fd-e17c35ae6b0d)

# Contributors
---
	Bakary Sylla, Yadisa Joiner, Marcus LeGare, Patrick Jones

# License
---
MIT

bsufdotv