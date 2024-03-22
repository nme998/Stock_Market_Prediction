# Stock_Market_Prediction
AI systems Project on predicting the stock market.

Dataset:
```
import datetime
import yfinance as yf

# We need to agree on specific timeframe
# end_date = ...
end_date = datetime.datetime.now() 
start_date = end_date - datetime.timedelta(days = 365 * 5)
stock_data = yf.download('TSLA', start=start_date.date(), end=end_date.date())

# Use only the 'Close' column for label (index 1)
data = pd.DataFrame(stock_data[['Open', 'Close', 'High', 'Low']].values, columns=['Open', 'Close', 'High', 'Low'])

```
