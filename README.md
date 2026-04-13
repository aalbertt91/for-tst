# Telegram Stock Price Alert Bot

This repository contains a Python-based automation tool designed to monitor live stock prices and send real-time alerts via Telegram. It tracks price volatility and triggers instant notifications when specific market thresholds are met, ensuring timely decision-making.

# 📌 Problem & Solution
Monitoring stock price movements manually throughout the trading day is inefficient and increases the risk of missing critical entry or exit points. Professional traders need an automated system that provides instant alerts without constant screen monitoring.

This automation bot:

Eliminates the need for manual price tracking by fetching live market data via the Yahoo Finance API.

Calculates real-time percentage changes relative to the previous day's closing price.

Automates instant notifications through the Telegram Bot API to ensure immediate awareness of price surges.

Implements structured logging and environment variable security to maintain a reliable and professional-grade monitoring tool.

# 🛠 Tech Stack
**Python:** Core programming for automation and API orchestration.

**yFinance:** For fetching historical and live financial market data.

**Requests:** To handle communication with the Telegram Bot API.

**Python-dotenv:** For secure management of sensitive credentials (API tokens).

**Logging:** To monitor execution flow, price checks, and alert status.

## ⚙️ Core Automation Workflow
**Initialization:** Loads secure credentials and fetches the previous day’s closing price for the target ticker.

**Monitoring:** Runs a continuous loop to download live price data at 5-minute intervals.

**Calculation:** Compares the live price against the benchmark to determine the percentage volatility.

**Notification:** Triggers a Telegram alert if the price change exceeds the defined threshold (e.g., 1%) and logs the event.

# 📊 Example Output
When the script is executed, it provides a real-time log of the monitoring process in the terminal:

```
INFO:root:Price alert bot started for AMD
Previous close price: 236.63999938964844
INFO:root:Successfully fetched previous close price for AMD: 236.63999938964844
/home/runner/workspace/telegram_price_alert_bot/src/price_alert_bot.py:37: FutureWarning: YF.download() has changed argument auto_adjust default to True
  data = yf.download("AMD", period="1d", interval="1m")
[*********************100%***********************]  1 of 1 completed
Live price: 245.02000427246094
INFO:root:Live price fetched for AMD: 245.02000427246094
Percentage change: 3.541246%
INFO:root:Price change calculated for AMD: 3.5412%
INFO:root:Price threshold reached for AMD: change=3.54%
INFO:root:Telegram alert sent successfully for AMD
INFO:root:Waiting 300 seconds before next price check
```

# 🚀 How to Run
1.Place your .env file in the project root folder with your BOT_TOKEN and CHAT_ID.

2.Install dependencies:

```
pip install -r requirements.txt
```
3.Run the automation:

```
python src/telegram_price_alert_bot.py
```
