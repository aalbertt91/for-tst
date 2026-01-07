Stock Market Data ETL Pipeline (YFinance → SQLite)
Project Objective
This project automates the extraction, transformation, and loading (ETL) of historical stock market data using the yfinance API and stores the processed data in a SQLite database. In addition, it generates basic financial summaries for selected stocks, such as daily price changes, average closing prices, and volatility metrics. The project aims to create a clean, reusable data pipeline suitable for basic financial analysis and reporting.

Technologies Used
Python: Core programming language used for data processing and automation.

Pandas: For data cleaning, manipulation, and numerical analysis.

Yfinance: For retrieving historical stock market data from Yahoo Finance.

SQLAlchemy: For ORM-based database interaction.

SQLite: Lightweight relational database used for storing stock price records.

Logging: To track execution flow and capture potential runtime issues.

Datetime: For handling date ranges and time-based operations.

How to Run
Ensure the required Python libraries are installed:

Bash

pip install -r requirements.txt
Run the script:

Bash

python src/stock-market-data-bot.py
After execution, check the financial_data.db SQLite database to verify that stock market data has been successfully inserted.

Why This Is Valuable for a Hedge Fund
This project is valuable for a Hedge Fund because it automates the retrieval of historical market data and ensures its integrity within a structured database for analysis and reporting.

By generating automated financial summaries (volatility, price changes, and averages), it provides immediate insights into market trends, reduces human error in data handling, and establishes a reliable foundation for more complex financial modeling and algorithmic trading strategies.
