# Stock Market Data ETL Pipeline (YFinance → SQLite)

## Project Objective

This project automates the extraction, transformation, and loading (ETL) of historical stock market data using the yfinance API and stores the processed data in a SQLite database. In addition, it generates basic financial summaries for selected stocks, such as daily price changes, average closing prices, and volatility metrics. The project aims to create a clean, reusable data pipeline suitable for basic financial analysis and reporting.

## Technologies Used

**Python:** Core programming language used for data processing and automation.

**Pandas:** For data cleaning, manipulation, and numerical analysis.

**Yfinance:** For retrieving historical stock market data from Yahoo Finance.

**SQLAlchemy:** For ORM-based database interaction.

**SQLite:** Lightweight relational database used for storing stock price records.

**Logging:** To track execution flow and capture potential runtime issues.

**Datetime:** For handling date ranges and time-based operations.

## How to Run

1. Ensure the required Python libraries are installed:

pip install -r requirements.txt

2. Run the script:

python src/stock-market-data-bot.py

3. After execution, check the financial_data.db SQLite database to verify that stock market data has been successfully inserted.

## Why This Is Valuable for a Hedge Fund

- Retrieves historical stock market data automatically from Yahoo Finance.
- Stores data in a structured SQLite database for reliable analysis and reporting.
- Generates automated financial summaries including daily changes and volatility metrics.
- Reduces manual data collection effort and ensures high data integrity for financial modeling.


--------

# Automated PDF Trade Report Extraction and Excel Conversion

## Project Objective

This project automates the extraction of trade-level and transaction data from financial PDF reports (such as broker statements and trade summaries) and converts them into clean, structured Excel files suitable for analysis and reporting. The pipeline is specifically designed to handle unstructured data, borderless tables, and column shifting issues common in financial documents, ensuring high data integrity for audit and reconciliation purposes.

## Technologies Used

**Python:** Core programming language used for the extraction engine and automation.

**Pdfplumber:** For deep-level text extraction and coordinate-based parsing of PDF content.

**Pandas:** For data structuring, deduplication, and numerical analysis.

**Regex (Regular Expressions):** To identify transaction rows and filter out headers/footers.

**Numpy:** For handling missing values (NaN) and maintaining data type consistency.

**Openpyxl:** Engine for generating professional Excel workbooks.

## How to Run

1.	Ensure the required Python libraries are installed:

pip install -r requirements.txt

2.	Run the script:

python pdf_to_excel_bot.py

3.	After execution, check the terminal for the Data Validation Report and verify the generated Trade_Statement_Analysis.xlsx file.

## Why This Is Valuable for a Hedge Fund

-	Operational Efficiency: Eliminates manual data entry, reducing human error and saving significant back-office resources.
-	Advanced Data Integrity: Uses a floating-point tolerance check (< 0.0001) to detect and fix column shifting issues that standard OCR tools miss.
-	Audit-Ready Reporting: Provides a clean, deduplicated, and normalized (BUY/SELL sides) trade log essential for risk management.
-	Scalability: The regex-driven logic allows processing of multi-page statements without structural breakdown.

---

# Portfolio Tracker & PnL Monitoring Bot

## Project Objective

This project is a Python-based portfolio tracking and profit & loss (PnL) monitoring system designed to automate the collection of market prices, store historical price data, calculate portfolio performance metrics, and generate automated reports and alerts.

The system retrieves near real-time (intraday) and historical stock prices using the yfinance API, stores daily price snapshots in a SQLite database, calculates daily and total PnL based on portfolio positions, generates Excel reports, and sends Telegram alerts when predefined PnL thresholds are exceeded.

The project aims to simulate a lightweight portfolio monitoring tool similar to those used in professional trading and risk management environments and is intended as a simplified prototype and learning-oriented system rather than a production trading platform.

## Technologies Used

Python: Core language for data processing, automation, and orchestration.

Pandas: Used for data manipulation, portfolio calculations, and report generation.

Yfinance: Retrieves intraday and historical stock market prices from Yahoo Finance.

SQLAlchemy: ORM-based interaction with the SQLite database.

SQLite: Lightweight relational database for storing daily stock price snapshots.

Logging: Tracks execution flow, database operations, and alert conditions.

Requests: Sends HTTP requests to the Telegram Bot API for automated PnL alerts.

Excel (openpyxl): Generates structured portfolio performance reports.

Dotenv: Manages sensitive configuration values such as API tokens.

## How to Run

1. Install the required dependencies:

pip install -r requirements.txt


2. Configure environment variables in a .env file:

BOT_TOKEN=your_telegram_bot_token
CHAT_ID=your_chat_id


3. Run the portfolio tracker script:

python src/portfolio_tracker.py


4. After execution, check the SQLite database (financial_data.db) for stored stock prices, review the terminal output for portfolio PnL calculations, verify the generated portfolio_report.xlsx file, and confirm that a Telegram alert is sent if the defined PnL threshold is exceeded.

## Why This Is Valuable for a Hedge Fund

- Automates portfolio monitoring and reduces manual tracking effort

- Demonstrates end-to-end data flow: API → database → analytics → reporting → alerts

- Simulates real-world portfolio PnL calculation logic

- Provides a foundation for:

   - Risk monitoring

   - Strategy performance tracking

   - Alert-driven decision-making

- Easily extensible to larger portfolios, additional asset classes, or scheduled execution

