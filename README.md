# Stock Price Analysis App

This is a simple Python app built with Streamlit and yfinance that allows users to analyze historical stock data. Users can select a ticker symbol from a predefined list and specify a date range to explore stock price and volume trends.

## Features

- **Ticker Selection:** Choose from a list of popular ticker symbols.
- **Date Range Selection:** Select a start and end date for historical data analysis.
- **Data Overview:** Get an overview of the selected stock's historical data statistics.
- **Interactive Charts:** Visualize historical stock price and volume trends through interactive line charts.

## How to Use

1. **Select Ticker:** Pick a ticker symbol from the dropdown list.
2. **Choose Date Range:** Set the start and end dates for the historical data.
3. **Explore Data:** Analyze stock data overview and visualize trends using the provided charts.

## Notes

- In case no data is found for the selected ticker or date range, a warning will be displayed.
- Users might encounter occasional errors due to connectivity or data unavailability issues.

## Why it exists

A small practice project to try Streamlit and the `yfinance` library: a few lines of Python become a working web app. It started from Streamlit's starter template (that is why `Finance.py` still carries Streamlit's Apache 2.0 license header).

## How to run it

```bash
pip install -r requirements.txt
streamlit run Finance.py
```

Then open http://localhost:8501. It needs an internet connection, since prices come live from Yahoo Finance through `yfinance`. There is also a `.devcontainer` for GitHub Codespaces.

## What is in here

- `Finance.py`: the whole app
- `requirements.txt`: dependencies (I added `yfinance`, which the app imports but was missing from the list)
- `.devcontainer/`: Codespaces setup (now points at `Finance.py` instead of a leftover `Hello.py`)

## What I learned

Streamlit makes a web UI with almost no web code, and a `try/except` around a network call is not optional. Also that stock tickers change: some in the dropdown (`FB`, `TWTR`) have been renamed or delisted, so they will show the "no data" warning.

## Heads-up

- Not financial advice, just a chart toy.
- No license file for my own code yet, so by default all rights are reserved there.
- I have not run the app again after tidying the repo.
