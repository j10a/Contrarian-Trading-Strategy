# Contrarian-Trading-Strategy

This code shows the backtesting of a contrarian strategy of “selling the winners and buying the losers.” The initial hypothesis is that stocks that performed well for the past day will decline the next day and stocks that fell the past day will increase.

Here, all returns are log returns (i.e., continuously compounded), and they are adjusted for corporate actions such as splits and dividends.

Let the return on stock i in period t be Ri(t) and define a “market index” to be given by the equal-weighted average return of all N stocks in the universe,

R(t)≡ 1/N sum(Ri(t)). (1)

At (or near) the end of period t, the excess return of security i above the mean is Ri(t)−R(t). Use this excess return to define a trading signal,

si(t) = −  Ri(t) − R(t)  , (2)
that can be used to rank order to candidate stock trades. A simple strategy consists of going long the top decile of stocks according to this signal and shorting the bottom decile. Neglect transaction costs, and rebalance the portfolio at the end of each day so that it holds the desired positions for the following tradedate. The individual weights wi(t) may be positive or negative, corresponding to long or short stock positions. Overall, the longs and shorts are balanced if  i wi(t) = 0.
In addition to specifying the sign of the weights, let’s further require that the stocks within each decile be equally weights and that the long/short portfolio be “fully-invested” by choos- ing the wi(t) on each day so that the sum of the long weights and the sum of the short weights separately add up to 100%.
That is,
 wi =1= |wj|. (3) i∈L j∈S
 
    The time series of daily portfolio returns, π(t) is given by
π(t)=∆MV = wi(t−1)Ri(t). (4)

 MV i∈U
