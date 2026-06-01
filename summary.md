**Summary**

## Methodology

• We worked with two datasets. The first was a trade-level dataset containing over 60,000 rows of real crypto trades, each with a timestamp, account ID, position size in USD, and closed PnL.

• The second was the Crypto Fear & Greed Index, a daily sentiment score that classifies market mood into five categories: Extreme Fear, Fear, Neutral, Greed, and Extreme Greed.

• Both datasets were cleaned. Missing values were checked, duplicates were removed, and zero PnL rows (open or flat trades) were identified.

• Timestamps were standardised and both datasets were joined on date so every trade carried the sentiment label for that day.

• From there, three layers of analysis were run:
• First, we looked at whether raw performance — PnL and win rate — differed across sentiment categories.
• Second, we examined whether trader behaviour itself changed with sentiment: did they trade more, size up, or shift their long/short bias?
• Third, we segmented traders into groups — profitable vs non-profitable, consistent vs inconsistent, frequent vs infrequent — and measured how each group responded to sentiment shifts.

## Insights

### Non-profitable traders bleed on Greed days

• The sharpest losses in the dataset cluster around Greed and Extreme Greed days, and they are driven almost entirely by non-profitable traders.

• On these days, this group increases their average position size and shifts heavily long chasing momentum at exactly the point where the market is most overheated.

• The result is larger losses, not larger gains.

### Profitable traders are sentiment-neutral

• Profitable traders show no meaningful performance difference across sentiment categories.

• Their PnL, win rate, and position sizing remain stable whether the market is in Extreme Fear or Extreme Greed.

• This is not because they are lucky — it is because their decisions are not driven by market mood.

### Consistency is the real edge

• When traders were split by win rate stability, the pattern was clear.

• Traders with a low standard deviation in their daily win rate held their performance across all sentiment conditions.

• Traders with a high standard deviation, those whose win rate jumps around from day to day, showed the worst outcomes during extreme sentiment periods in both directions.

• Extreme Fear hurt them.

• Extreme Greed hurt them.

• The inconsistency was the problem, not the sentiment itself.

### More trades during extreme sentiment means worse outcomes

• Trade volume rises noticeably during Extreme Fear and Extreme Greed periods.

• But average PnL per trade falls.

• Traders are reacting to the market by doing more, and that activity is costing them.

• The data shows no evidence that increasing trade frequency during emotional market conditions produces better results.

### Long bias spikes on Greed days

• The long/short ratio shifts significantly toward long during Greed periods across the full trader population.

• Non-profitable traders show this pattern most strongly.

• They are not hedging or staying neutral — they are piling into longs at market peaks and absorbing the drawdown when sentiment reverses.

## Strategy Recommendations

### Size down on Greed and Extreme Greed days

• The data is unambiguous here.

• Non-profitable traders take their biggest losses when they are most aggressive, and they are most aggressive when the market is greedy.

• Cutting position size on Greed days directly targets the single biggest source of loss in this dataset.

• This does not require predicting the market — it only requires reacting to a publicly available daily index.

### Cap your trade count during extreme sentiment

• There is a consistent pattern across the dataset: volume goes up during Extreme Fear and Extreme Greed, and average PnL per trade goes down.

• The practical rule is simple — do not exceed your normal daily trade count during extreme sentiment periods.

• More trades under emotional conditions does not create more edge.

• It compounds mistakes.

### Stop reacting to sentiment, start following a process

• The traders who performed best across this entire dataset, across every sentiment category, across all time periods, were the consistent ones.

• Not the most profitable on any single day, but the most stable over time.

• They likely follow fixed entry and exit rules that do not bend based on what the Fear & Greed Index says.

• Building that kind of process is what separates the profitable segment from the rest, and no amount of sentiment-reading will substitute for it.

## Limitations

• Sentiment is assigned as a single daily label, meaning all trades placed on a given day carry the same classification regardless of whether they were placed at market open or close.

• Intraday sentiment shifts are not captured.

• Trader segments are defined using the full dataset, so the analysis describes historical patterns rather than offering a predictive framework.

• A trader labelled non-profitable here was assessed on the same data used to measure their sentiment-day performance.

• The segments cannot be used to make forward-looking claims without a proper train/test split across time.

• Mean PnL figures are sensitive to outliers.

• A small number of very large winning or losing trades can shift the average significantly.

• All numerical findings should be read as directional patterns rather than precise benchmarks.
