# SK_put_spread
micro project to price a CBOE S&P 500 Index Option spread

This project will seek to construct, price, evaluate and roll a two-legged ratio put back spread using the S&P 500 Index Options traded on the CBOE.

The required set of positions for the required spread is driven by the following logic:

Sell the 1 week ATM puts at the Friday open. With the proceeds of the short 1 week, ATM put purchase 3 puts with at least 90 days to expiration in a deferred expiration cycle.
Roll the longer-dated long put leg of the position if the S&P 500 rallies sufficiently to cause the OTM puts to move to > = 15% OTM or roll the longer-dated long put leg and the short-dated, short put positions if the S&P 500 declines sufficiently to cause the OTM puts to become > = 5% ITM.
If the S&P 500 enters a Bear Market as defined by declining below by the 10-month moving average add 1 short synthetic futures position to the portfolio holding until the S&P 500 regains the 10-months moving average.
We will require a daily evaluation in dollar terms of the aggregate position for each day in the evaluation period.
