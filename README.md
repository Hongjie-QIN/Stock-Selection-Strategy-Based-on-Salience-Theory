# Stock-Selection-Strategy-Based-on-Salience-Theory

1. Hypothesis
According to the Salience Theory, stocks with a return rate that is too low than the market return rate will cause investors to panic, cause the market to overreact, and investors to over-sell, making the stock price likely to increase in the future.

2.Factor Construction
1) Panic Degree
According to the research report construction method, we construct the “panic degree” as follows:
1.Take the return of the CSI 1000 Index as a representative of the market level, while taking the daily return rate of the CSI 1000 Index (today's closing index/yesterday's closing index -1) as today's market return level.
2.Calculate the difference between the stock return rate and the market return rate, and then take the absolute value as the deviation level of the individual stock relative to the market return rate, recorded as the "deviation item"; calculate the absolute value of the individual stock return rate, and add the absolute value of the market return rate. Take the value plus 0.1 as the overall market return level, recorded as the “base item”.
3.Use the “deviation term” to divide the “base term” to get the “panic degree” of the stock on that day.

2) “Primal Panic” Factor
Based on the “Panic Degree” factor, we construct the “primal panic” factor:
1.Use the daily stock return rate (today's closing/yesterday's closing -1) directly as the decision-making score for the stock of the day.
2.Multiply the daily “Panic Degree” by the daily rate of return to obtain the weighted-adjusted decision score, referred to as the “weighted decision score”.
3.At the end of each month, calculate the mean and standard deviation of the “weighted decision score” of the past 20 trading days, respectively, as improvements to the “20-day yield factor” and “20-day volatility factor”, respectively, recorded as the “panic return” factor and the “panic volatility” factor are equal-weighted and synthesized into the “primal panic” factor.
4.The “panic return” factor, “panic volatility” factor and “primal panic” factor constructed above were tested in the all-A sample at monthly (Freq=20) and daily (Freq=1) frequencies. During the test, the market value and industry orthogonalization of the factors were performed, and the test interval was 2017/1/1 to 2022/12/31.
5.“Step1_calculate_factors.ipynb” is the procedure of factor calculating, and backtesting procedures are “Step2_simple_backtest_factor_score_freq=20.ipynb” (monthly factor) and “Step2_simple_backtest_factor_score_freq=1.ipynb” (daily factor). The backtesting results for the “panic return” factor and “panic volatility” factor are shown in the Appendix.
