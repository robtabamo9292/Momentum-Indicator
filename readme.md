### What it does

Plotsa smoothed “fair value” centerline:
- **Center**: kernel regression (fair value)
- **Buy Line**: lower band (oversold/dip zone)
- **Sell Line**: upper band (overextension zone)  
Adapts automatically to **any timeframe** and **any token’s volatility**.

### Signals
- **BUY (Early):** price enters the **lower band zone** + momentum **turns up** (before the big move).
- **SELL (Momentum Loss):** price is **elevated** (above center by default) + momentum **turns down** (first sign of fade).
- **Bull vs Bear Buy:**  
  - **Bull Buy:** above trend EMA (optionally EMA slope up)  
  - **Bear Buy:** outside bull regime (treat as mean reversion / smaller targets)

### Key settings
- **Envelope Lookback (days):** higher = smoother/fewer signals; lower = faster/more signals  
- **Band Multiplier:** lower = earlier/more trades; higher = cleaner/fewer trades  
- **Buy Zone:** `Touch Lower Band` (earliest) vs `Close Below` (stricter)  
- **Sell Zone:** `Above Center` (earlier exits) vs `Touch Upper Band` (later exits)  
- **Band Mode:** `ATR+MAE` (recommended)  
- **Momentum Engine:** `MACD` (recommended) or `RSI`

### Recommended defaults (general crypto)
- Lookback: `14`
- Band Mult: `2.3`
- Band Mode: `ATR+MAE`
- Buy Zone: `Touch Lower Band`
- Sell Zone: `Above Center`
- Momentum: `MACD`
- Trend slope filter: `ON`

### Quick tuning (too much chop)
- Band Mult `+0.2` (e.g., 2.3 → 2.5)
- Lookback `+3–5 days` (e.g., 14 → 18)
- Consider `Close Below Lower Band`
