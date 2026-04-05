https://www.kaggle.com/datasets/prasad22/healthcare-dataset



vLIWXkLtYgdL7RSDUWV3





cluster\_data = \[]

tickers = df\['ticker'].unique()



for ticker in tickers:

&#x20;   ticker\_subset = df\[df\['ticker'] == ticker].copy()

&#x20;   

&#x20;   # percentage change in daily price

&#x20;   ticker\_subset\['daily\_close'] = ticker\_subset\['close'].pct\_change()

&#x20;  

&#x20;   # calculations

&#x20;   mean\_daily\_close = ticker\_subset\['daily\_close'].mean()

&#x20;   std\_daily\_clos = ticker\_subset\['daily\_close'].std()

&#x20;   

&#x20;   cluster\_data.append({

&#x20;       'ticker': ticker,

&#x20;       'mean\_daily\_close': mean\_daily\_close,

&#x20;       'std\_daily\_clos': std\_daily\_clos,

&#x20;   }).

juo-ivfy-mri

