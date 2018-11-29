# SK_put_spread
micro project to price a CBOE S&amp;P 500 Index Option spread

This project will seek to construct, price, evaluate and roll a two legged ratio put back spread using the S&P 500 Index Options traded on the CBOE.

The required set of postions for the required spread is driven by the following logic:
  1. Sell the 1 week ATM puts at the Friday open. With the proceeds of the short 1 week ATM put purchase 3 puts with at least 90 days to expiration in a deferred expiration cycle.
  2. Roll the longer dated long put leg of the position if the S&P 500 rallies suffciently to cause the OTM puts to move to > = 15% OTM or roll the longer dated long put leg and the short dated, short put postions  if the S&P 500 declines sufficently to cause the OTM puts to become > = 5% ITM.
  3. If the S&P 500 enters a Bear Market as defined by declining below by the 10 month moving average add 1 short synthetic futures position to the portfolio holding until the S&P 500 regains the 10 month moving average.
  
  We will require a daily evalutation in dollar terms of the aggrate position for each day in the evaluation period.
