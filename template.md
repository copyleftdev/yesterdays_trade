# If I Traded Yesterday: [Stock Symbol/Company] - [Date]

*Brief engaging introduction paragraph (2-3 sentences) summarizing the stock’s major move.*

## Why [Stock Symbol] Was a Profitable Day-Trading Candidate

- **News Catalyst:** Clearly state what news triggered the price movement (earnings, approvals, industry events, etc.).
- **Technical Setup:** Describe key technical signals (gap up/down, unusual volume spike, breakout levels, etc.).
- **Market Context:** Briefly highlight additional factors influencing trading behavior (short interest, retail interest, sentiment, etc.).

## Trading Strategy Used

### Step-by-step Breakdown:
1. **Identifying Trade Setup** (e.g., Momentum, Breakout, News-based)
2. **Technical Entry Criteria** (MACD cross, RSI threshold, volume spike, VWAP bounce/break)
3. **Risk Management:** Clearly define stop-loss placement and initial risk.
4. **Exit Criteria:** Define when to exit based on technical indicators or price targets.

## Technical Trade Execution Details

- **Entry Point:** (exact entry price, indicator levels at entry)
- **Exit Point:** (exact exit price, reason for exit)
- **Indicators Confirmation:**
  - RSI levels at entry/exit
  - MACD crossover moments
  - VWAP behavior (support/resistance)
  - Volume pattern & confirmation

*Include annotated visualization/chart (if available): clearly mark entry/exit and indicators.*

## Simulated Trade Results

| Metric                | $1,000 Position | $10,000 Position | $100,000 Position |
|-----------------------|-----------------|------------------|-------------------|
| Entry Price           | `$XX.XX`        | `$XX.XX`         | `$XX.XX`          |
| Exit Price            | `$YY.YY`        | `$YY.YY`         | `$YY.YY`          |
| Number of Shares      | `ZZ`            | `ZZZ`            | `ZZZZ`            |
| Total Profit/Loss     | `$AAA (+/- %)`  | `$BBB (+/- %)`   | `$CCC (+/- %)`    |

## Strategy in Pseudocode (Algorithmic Trader Reference)

```pseudo
function TradeYesterday(stock):
    news = CheckSignificantNews(stock)
    if not news:
        return "No actionable news, skip stock."

    data = GetIntradayData(stock)
    opening_range = GetOpeningRange(data, minutes=15)
    breakout_level = opening_range.high
    indicators = CalculateIndicators(data, ["RSI", "MACD", "VWAP"])

    if (PriceBreaksAbove(data, breakout_level) and
        indicators.MACD.isBullishCross and
        indicators.RSI.crossesAbove(60) and
        VolumeSpikeAboveAverage(data)):

        entry_price = breakout_level
        stop_loss = indicators.VWAP.price * 0.97

        shares = CalculateShares(available_capital, entry_price)
        position = EnterLong(stock, shares, entry_price, stop_loss)

        while market_is_open:
            current_data = UpdateIntradayData(stock)
            current_indicators = UpdateIndicators(current_data)

            if (RSIDivergence(current_indicators) or
                MACDHistogramDeclines(current_indicators) or
                PriceBreaksBelow(VWAP)):
                exit_price = current_data.price
                ExitLong(position, exit_price)
                break

        profit_loss = CalculatePL(entry_price, exit_price, shares)
        return profit_loss
    else:
        return "No valid breakout entry triggered."
```

## Key Takeaways and Lessons Learned

- Brief summary of actionable insights gained from this specific trade.
- Important technical observations or market behaviors.
- Suggestions for similar future trade setups.

Stay tuned for tomorrow’s "If I Traded Yesterday," where we’ll analyze another profitable trading opportunity!

