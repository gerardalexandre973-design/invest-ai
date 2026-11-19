INVEST AI Technical Indicators Engine v1
Purpose
Generate technical indicators from historical price data.

SMA (Simple Moving Average)
SMA20
Average close price of last 20 trading sessions.

SMA50
Average close price of last 50 trading sessions.

SMA100
Average close price of last 100 trading sessions.

SMA200
Average close price of last 200 trading sessions.

EMA (Exponential Moving Average)
EMA12
Exponential average of last 12 sessions.

EMA26
Exponential average of last 26 sessions.

RSI14
Period: 14 trading sessions.

Formula:

RS = Average Gain / Average Loss

RSI = 100 - (100 / (1 + RS))

MACD
MACD = EMA12 - EMA26

Signal = EMA9(MACD)

Bullish: MACD > Signal

Bearish: MACD < Signal

ATR
Average True Range

Period: 14 sessions

Purpose: Measure volatility.

ADX
Period: 14 sessions

Purpose: Measure trend strength.

Interpretation:

ADX < 20 → Weak Trend

20-25 → Moderate Trend

25 → Strong Trend

OBV
On Balance Volume

Purpose: Measure accumulation/distribution.

Relative Volume
Current Volume / Average Volume (20 sessions)

RVOL > 1.3 = positive signal

Minimum History Requirements
SMA20 → 20 sessions

SMA50 → 50 sessions

SMA100 → 100 sessions

SMA200 → 200 sessions

Indicators requiring unavailable history must return NULL.

Data Quality Rules
Missing prices: Do not calculate indicator.

Less history than required: Return NULL.

Zero volume: Log warning.
