What the Bot Does

Scans 15-minute price action for STRAT candle sequences (e.g., 2-1-2, 3-1-2, 1-2-2, 2-2, 3-2-2)

Posts Discord alerts with:

Pattern + direction (Bullish/Bearish)

Underlying price

Suggested options contract (Call/Put, strike, expiry)

Bid/Ask, OI, option volume, IV

Greeks (Delta/Theta/Gamma/Vega when available)

Exit plan: SL + TP1/TP2/TP3 (stock-based levels)

Context signals (trend/volume/earnings/correlation)

Confidence grade (A+ → C+) based on historical outcomes

Renders an optional candlestick chart image highlighting the STRAT window (last 3 candles)

Key Features
✅ STRAT Pattern Detection

Candle classification: 1 (inside), 2u (up), 2d (down), 3 (outside)

Pattern matching for common STRAT sequences including:

3-1-2 reversals

2-1-2 continuation/reversal

1-2-2 rev strat

2-2 continuation/reversal

3-2-2 reversals

✅ Options Contract Suggestion + Greeks

Pulls the nearest expiry chain and selects a strike nearest to spot (ATM-ish)

Extracts Bid/Ask, OI, Volume, IV

Computes Greeks via Black–Scholes when IV is available:

Delta, Theta, Gamma, Vega

✅ Signal Context (Added to Alerts)

These do not necessarily block an alert, but provide better decision support:

Volume spike detection vs recent 15m average

1H trend confirmation (e.g., price vs 1H EMA20)

Sector correlation alignment using SPY/QQQ reference moves

Earnings proximity warnings (e.g., earnings within ~3 trading days)

Fibonacci confluence labeling (display-only confluence)

✅ Confidence Grading System (A+ → C+)

Each alert includes a confidence score based on stored results:

Pattern historical win rate (weighted)

Ticker historical win rate (weighted)

Filter/quality component (expandable)

✅ Outcome Tracking + Learning (Database-backed)

The bot logs detections into a database and later records outcomes at multiple checkpoints:

+15m / +30m / +45m / +1h / +2h / +4h

Captures close + intrabar high/low so you can evaluate wicks and drawdowns

✅ Automation + Manual Control

Auto-scheduled scans during market hours

Manual “Run Signal Check” button in Discord

Commands for testing and performance reporting (examples):

!test (sample alerts)

!stats (filter and performance summary)

Market Hours / Holiday Logic

The scanner is designed to skip:

Weekends

US market holidays

Outside market hours

Half-day closes (e.g., day after Thanksgiving, Christmas Eve) with early close behavior

Architecture Overview

High-level flow:

Scheduler triggers a scan (e.g., every 15 minutes during market hours)

For each ticker:

Download recent 15m data

Detect STRAT pattern

Choose option contract + compute Greeks

Compute context signals (volume spike, trend, correlation, earnings, fib confluence)

Compute exits (SL/TPs)

Log to DB

Compute confidence grade from historical outcomes

Render chart image (optional)

Send Discord alert

Outcome tracking job runs periodically to backfill results for grading and optimization

Weekly optimizer job tunes configuration and suppression rules over time (optional)

Tech Stack

Python

Market data / options chains: yfinance

Data processing: pandas, pandas_ta

Discord bot + UI: discord.py

Scheduling: APScheduler

Charting: mplfinance, matplotlib (headless mode)

Options math: py_vollib (Black–Scholes + Greeks)

Holidays/time: holidays, pytz

Persistence + learning: SQLite (via custom database.py module)

Repository Status / Source Code Access

🔒 Private Codebase
The full source code is private to protect proprietary logic and implementation details. If you are:

a recruiter,

a potential collaborator,

or you’d like a demo / architecture walkthrough,

please reach out and I can share a walkthrough, sample outputs, or discuss the system design.

Screenshots

Add screenshots here (recommended):

Discord alert example

Chart example with STRAT candle labels

Example:

<img width="571" height="663" alt="image" src="https://github.com/user-attachments/assets/103fd318-15e6-4c19-85a4-761561595ffa" />


Roadmap (Optional)

Add multi-timeframe scanning (5m/30m/1h) as confirmers

Improve exit logic (ATR, structure-based stops, R-multiples)

Improve grading model (separate scoring for trend-aligned vs countertrend)

Replace yfinance with a faster data source for reliability

Add slash commands and richer Discord UI

Disclaimer

This project is for educational and research purposes only and is not financial advice. Trading involves risk. You are responsible for any decisions made using these outputs.

Contact

If you want to connect or see a demo:

LinkedIn:(https://www.linkedin.com/in/clarence-burnett/)

GitHub:(https://github.com/DonClaro/strat-trading-bot-showcase)

Discord: https://discord.gg/szXvcmYA
