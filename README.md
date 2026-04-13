# Macro News Automation Pipeline

This repository contains a Python-based data pipeline designed to automate the extraction, transformation, and reporting of macroeconomic news from the official Federal Reserve XML feed. The system parses high-impact press releases, structures unstructured XML data, and delivers automated intelligence reports via email.

# 📌 Problem & Solution

Monitoring central bank communications and policy shifts manually is a bottleneck for macro strategy teams. Missing a high-impact Federal Reserve announcement can lead to significant market risk, yet manual tracking of XML feeds and press releases is inefficient.

This automation bot:

Eliminates manual monitoring by automatically fetching the latest press releases from official Federal Reserve feeds.

Transforms raw, hierarchical XML data into clean, tabular DataFrames for structured analysis.

Streamlines reporting by generating formatted Excel workbooks for long-term news tracking.

Enhances operational efficiency by delivering real-time reports via secure SMTP email automation to stakeholders.

# 🛠 Tech Stack
**Python:** Core orchestration and pipeline automation.

**Requests:** For secure ingestion of official Federal Reserve XML feeds.

**ElementTree (XML):** For high-precision parsing of structured macro data.

**Pandas:** For data transformation and tabular structuring.

**Openpyxl:** To generate professional Excel-based tracking reports.

**Smtplib / EmailMessage:** For automated and secure email delivery protocols.

**Dotenv:** For managing sensitive email credentials and environment variables.

# ⚙️ Core Automation Workflow
**Ingestion:** Connects to the Federal Reserve RSS/XML feed to retrieve the latest policy communications.

**Parsing & Transformation:** Extracts relevant fields (Title, Date, Link) and cleans the data into a Pandas DataFrame.

**Report Generation:** Converts the processed macro data into a formatted Excel report.

**Automated Delivery:** Attaches the report and dispatches it to a predefined list of receivers via automated email.

# 📊 Example Output
Upon execution, the bot displays the processed macro items and confirms the delivery status:

```                                              title                         pubDate
0  Federal Reserve Board announces approval of ap...   Fri, 10 Apr 2026 20:15:00 GMT
1  Federal Reserve Board announces termination of...    Thu, 9 Apr 2026 15:00:00 GMT
2  Minutes of the Federal Open Market Committee, ...    Wed, 8 Apr 2026 18:00:00 GMT
3  Federal Reserve Board invites public comment o...    Wed, 8 Apr 2026 15:30:00 GMT
4  Federal Reserve Board issues enforcement actio...    Fri, 3 Apr 2026 15:00:00 GMT

[10 rows x 6 columns]
📧 Email sent successfully!
```


# 🚀 How to Run
1. Configure your .env file with SENDER_EMAIL, EMAIL_PASSWORD, and RECEIVER_EMAIL.

2. Install dependencies:

```
pip install -r requirements.txt
```


3. Run the automation:

```
python src/news_report_bot.py
```
