

# crypto-trading-research

I built 5 tools to understand crypto markets. Not tutorials. Real stuff that pulls live data.

## What's inside

**1. Orderbook analysis** - Checks BTC spread on Bybit. Right now it's 0.01 basis points. That's tight. About $2.1M sitting within 0.1% of current price. Good for market making.

**2. Funding rate tracker** - Watches Binance perpetual futures. Currently, shorts are paying 2.77% annualized to longs. That tells you market sentiment.

**3. Arbitrage scanner** - Looks at BTC across 5 exchanges (Binance, Bybit, OKX, Gate.io, KuCoin). Spread is 0.032% right now. Not enough to profit after fees. But DOGE shows 0.133% - wider spreads on memecoins.

**4. Backtesting** - Simple SMA crossover strategy on simulated data. Returned 0.68%. Nothing special. But the framework works.

**5. SQLite database** - Stores arbitrage results. In production, I'd use PostgreSQL with TimescaleDB.

## Why I built this

There's a lot of hype in crypto trading. "Arbitrage this" "Market making that." I wanted to see for myself.

What I found: BTC is efficient. You won't find free money there. But mid-caps and memecoins? Wider spreads. Real opportunities if you're fast enough.

## The contradiction nobody talks about

Everyone says, "Find arbitrage opportunities." But by the time you see the spread, it's usually gone. The real edge isn't spotting the arb - it's execution speed and fee management.

A 0.3% spread looks good until you pay withdrawal fees, exchange fees, and slippage. Then it's gone.


What I used
Python (requests, pandas, numpy, websockets)

Binance, Bybit, OKX, Gate.io, KuCoin APIs

SQLite for storage

Jupyter for everything

What's next
WebSockets for real-time (REST is too slow for actual trading)

PostgreSQL + TimescaleDB

More strategies (momentum, mean reversion)

Risk metrics (max drawdown, VaR)

The reality check
These tools won't make you rich. They're for learning how markets work. If you want to trade, you need execution infrastructure and serious capital.

But for a quant research role? This shows you know how to think about the problem.


Built in Nigeria with a VPN to Germany. Because crypto APIs are weird like that.


## How to run this

```bash
git clone [your repo URL]
pip install -r requirements.txt
jupyter notebook crypto-trading-research.ipynb

Then click "Run All Cells."
