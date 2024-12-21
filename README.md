Value at Risk (VaR) in finance basically describes the trade off between risk and return.

Though we have implementations such as std, variance, beta value to consider risk, these are not probability distribution.

There are couple of ways to calculate VaR - one being variance and other being Monte Carlo Distribution. 

In the variance method, we assume the daily returns are normally distributed meaning that the mean is 1 and the std is 0. However these would sometimes not apply to VaR as the VaR may not neccessarily look at risk for 1 day. 
Therefore, the confidence level is introduced where VaR can be calculated using critical value, std of returns and the time horizon. 

In the Monte Carlo simulation we have several realization of our investment using geometric random walks, then we sort the underlying realisations. We are after the percentile that we have defined using the confidence level
The difference between initial investment and the one at the percentile is the value of risk we are looking for. 

As you can see from both approaches, we have come to a similar answer of around 25k. This means that we have 95% confidence that we will loose around 25k if we invest 1,000,000 in Citi stock given the historical data between the given dates (2014-2017)

I have used Pandas to caluclate the VaR instead of Python due to ease of use. However these can be simulated in Python using OOP
