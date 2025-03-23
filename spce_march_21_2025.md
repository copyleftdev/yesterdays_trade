# If I Traded Yesterday: Virgin Galactic (SPCE) - March 21, 2025

Virgin Galactic (SPCE) soared nearly 40% on March 21, 2025, following FAA approval to fly paying customers to space, presenting a perfect day-trading opportunity.

## Why SPCE Was a Profitable Day-Trading Candidate

- **News Catalyst:** FAA approved SPCE for commercial space flights, sparking huge investor interest.
- **Technical Setup:** Significant premarket gap up (around 12%), breakout from previous resistance levels, record-breaking volume spike.
- **Market Context:** High short-interest (>20%) increased the potential for a short squeeze.

## Trading Strategy Used

### Step-by-step Breakdown:
1. **Identifying Trade Setup:** Momentum breakout strategy triggered by significant positive news and volume.
2. **Technical Entry Criteria:** Entry upon breakout above morning consolidation (~$48), confirmed by MACD bullish crossover and RSI crossing above 60.
3. **Risk Management:** Stop-loss set below morning support and VWAP (~$45).
4. **Exit Criteria:** Exit when RSI showed bearish divergence above 80, signaling momentum exhaustion around $55.

## Technical Trade Execution Details

- **Entry Point:** ~$48; RSI rising above 60; MACD bullish crossover confirmed.
- **Exit Point:** ~$55; RSI bearish divergence at ~85.
- **Indicators Confirmation:**
  - RSI stayed overbought through rally, divergence appeared signaling the exit.
  - MACD confirmed bullish momentum entry.
  - VWAP acted as intraday support.
  - Volume spike at breakout confirmed validity.

## Simulated Trade Results

| Metric                | $1,000 Position | $10,000 Position | $100,000 Position |
|-----------------------|-----------------|------------------|-------------------|
| Entry Price           | $48.00          | $48.00           | $48.00            |
| Exit Price            | $55.00          | $55.00           | $55.00            |
| Number of Shares      | 20              | 208              | 2083              |
| Total Profit          | $140 (14%)      | $1,456 (14%)     | $14,581 (14%)     |

## Strategy in Pseudocode (Algorithmic Trader Reference)

```pseudo
function TradeYesterday(stock):
    if not HasSignificantNews(stock):
        return "No news catalyst."

    data = FetchIntradayData(stock)
    opening_range = CalculateOpeningRange(data, minutes=15)
    breakout_price = opening_range.high
    indicators = CalculateIndicators(data, ["RSI", "MACD", "VWAP"])

    if PriceBreaksAbove(data, breakout_price) and indicators.MACD.isBullish and indicators.RSI.crossesAbove(60) and VolumeSpike(data):
        entry = breakout_price
        stop_loss = indicators.VWAP * 0.97

        shares = AllocateCapital(available_capital, entry)
        position = EnterTrade(stock, shares, entry, stop_loss)

        while TradingHours():
            data = UpdateIntradayData(stock)
            indicators = UpdateIndicators(data)

            if indicators.RSI.showsBearishDivergence() or PriceDropsBelow(indicators.VWAP):
                exit_price = data.currentPrice
                ExitTrade(position, exit_price)
                break

        return CalculateProfitLoss(entry, exit_price, shares)

    else:
        return "No trade executed."
```

## Key Takeaways and Lessons Learned

- Major news catalysts often lead to high-probability breakouts.
- Confirmation via multiple indicators (RSI, MACD, volume, VWAP) significantly improves entry accuracy.
- Always manage risk with clear stop-loss levels to preserve capital.

Stay tuned for tomorrow’s analysis in "If I Traded Yesterday" to discover another profitable setup!

