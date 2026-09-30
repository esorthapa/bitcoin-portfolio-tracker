# Bitcoin Portfolio Tracker (ETL)

A Python-based bitcoin portfolio tracking and ETL project that collects market data for Apple (AAPL) and Bitcoin, converts values into AUD, and calculates portfolio values based on provide link.

The project is being developed as a practical portfolio project to demonstrate skills in Python, REST APIs, ETL, data transformation, Pandas, SQL, data analysis, and visualization.




## Project Overview

The project follows an ETL-based architecture:

External APIs
     ↓
   Extract
     ↓
  Transform
     ↓
 Portfolio Data
     ↓
    Load
     ↓
Analysis & Visualization

The initi echnologies
.Python
.Jupyter Notebook / JupyterLab
.Pandas
.Requests
.python-dotenv
.REST APIs
.SQLite
.SQL
.Matplotlib
.Git


## Data Sources
#### CoinGecko
https://api.coingecko.com/api/v3/ping

Used to retrieve the current Bitcoin price in AUD.

#### Alpha Vantage
https://www.alphavantage.co/query

Used to retrieve daily Apple (AAPL) stock market data.

#### Frankfurter
https://api.frankfurter.dev/v2/rate/usd/aud

Used to retrieve the USD to AUD exchange rate.


## ETL Process
#### Extract

Market data is collected from external APIs:

Bitcoin price in AUD
AAPL price in USD
USD to AUD exchange rate

#### Transform

The extracted data is transformed to calculate:

AAPL price in AUD
AAPL portfolio value
Bitcoin portfolio value
Total portfolio value

The portfolio currently uses example holdings for:

AAPL
Bitcoin

#### Load

The next stage of the project will store portfolio snapshots in a SQLite database for historical analysis.

## Environment Configuration

API credentials are stored using environment variables.

Sensitive credentials are kept in .env and excluded from Git using .gitignore.

A .env.example file is included to show the required configuration without exposing API credentials.


## Project Structure
portfolio-tracker/
│
├── data/
│   └── backups/
│
├── logs/
│
├── charts/
│
├── Bitcoin_tracker.ipynb
├── .env.example
├── .gitignore
└── README.md

#### Directories

data/backups/
Stores CSV backups of portfolio data.

logs/
Stores application and ETL execution logs.

charts/
Stores generated portfolio charts and visualizations.

Bitcoin_tracker.ipynb
Main Jupyter Notebook containing the ETL and portfolio analysis workflow.

## Current Features
API integration with CoinGecko
API integration with Alpha Vantage
API integration with Frankfurter
Environment variable management
Error handling for API requests
Bitcoin price extraction
AAPL price extraction
USD/AUD exchange-rate extraction
Currency conversion
Portfolio value calculation
Portfolio summary
Git/GitHub version control


## Security

API keys and other sensitive information are stored locally in .env.

The .env file is excluded from GitHub using .gitignore.

Only .env.example is committed to the repository.

Never commit API keys, passwords, tokens, or other secrets to GitHub.

## Data Pipeline Progress
External APIs → Extract → Transform → Pandas DataFrame → Timestamped Portfolio Snapshot

The timestamped DataFrame will subsequently be stored in SQLite for historical analysis.


## Author

#####
Python | ETL | Data Analysis | APIs | SQL | Software Development



