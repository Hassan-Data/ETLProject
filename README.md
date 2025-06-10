📊 Stock Market Intelligence Dashboard
A Real-Time BI Project Using Python, PostgreSQL & Power BI

Python · PostgreSQL · Power BI · License

🚀 Overview
This project demonstrates a real-time Business Intelligence pipeline for the stock market. It fetches live or recent stock price data using a Python ETL script, loads and manages the data with PostgreSQL, and presents insights using Power BI. The pipeline is fully automatable via Task Scheduler.

🧰 Tech Stack
Tool	Purpose
Python	ETL Script (requests, pandas)
PostgreSQL	Data Storage
Power BI	Dashboard Visualizations
Task Scheduler	Automation

📂 Folder Structure
bash
Copy
stock-market-intelligence/
├── config/                  # .env file (API + DB settings)
├── scripts/                 # ETL script(s) (e.g., pipeline.py)
├── powerbi/                 # Power BI dashboard (.pbix)
├── etl_logs/                # Auto-generated logs
├── run_etl.bat              # Batch script for automation
├── requirements.txt         # Python dependencies
├── .gitignore
├── README.md
└── LICENSE
⚙️ ETL Process
Extract stock data using an API (e.g., Alpha Vantage, Yahoo Finance).

Transform data with pandas (select fields, clean data, compute new metrics).

Load into a PostgreSQL table called stock_listings_latest.

Example:

python
Copy
response = requests.get(api_url, params=params)
data = response.json()
# Transform, connect to DB, insert rows...
See full code: scripts/pipeline.py

📊 Power BI Dashboard Highlights
Visualizations Include:

📈 Line chart: Open vs. Close prices over time

🔝 Bar chart: Top performing stocks (e.g., by percent change)

🍩 Donut chart: Portfolio/stock distribution by market value or percent

💡 KPI Cards: Total volume, best/worst performers, averages

📋 Conditional table: Price changes & percent changes

➕ Green = Gain, ➖ Red = Loss

📈 Key Insights
See which stocks drive most of your portfolio’s performance

Track daily, weekly, or monthly volatility

Identify correlations between price, volume, and market movements

⚡ Setup & Usage
1. Clone the repo:

sh
Copy
git clone https://github.com/Abdulmohimen/ETLProject.git
cd ETLProject
2. Create your .env in /config:

ini
Copy
API_KEY=your_stock_api_key
DB_NAME=stockdb
DB_USER=postgres
DB_PASS=your_password
DB_HOST=localhost
3. Install dependencies:

sh
Copy
pip install -r requirements.txt
4. Run the ETL:

sh
Copy
python scripts/pipeline.py
5. Or automate it with:

sh
Copy
run_etl.bat
🔁 Automation
Task Scheduler runs run_etl.bat on a schedule (e.g., daily)

Logs saved to /etl_logs/etl_log.txt

📈 Future Enhancements
📉 ML-based stock trend forecasting

☁️ Host dashboard on Power BI Service

📬 Email/Telegram alerts on major market changes

🧑‍💻 Author
Abdulmohimen Elosta
EU Business School — Master's in Business Analytics & Data Science
[GitHub Project Link](https://github.com/Abdulmohimen/ETLProject/)

📄 License
MIT — use freely, credit appreciated.

