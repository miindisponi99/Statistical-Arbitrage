# Pairs trading strategy
Statistical arbitrage with cointegration is a trading strategy that aims to exploit the price relationship between two or more assets that exhibit a long-term equilibrium. Cointegration is a statistical property that suggests the assets' prices move together over time, even though they may have short-term price divergences.<br>

The process begins by identifying pairs of assets that are likely to be cointegrated. The cointegration function is used to calculate the p-values for cointegration between pairs of variables in a given dataset. Pairs with p-values below a certain threshold (in this case, 0.05) are considered to exhibit cointegration.<br>

Once the cointegrated pairs are identified, the pairs trading strategy is implemented. The code calculates the spread between the prices of the two assets in each pair. The spread represents the deviation from the long-term equilibrium between the assets.<br>

The strategy then calculates the z-score of the spread, which measures how many standard deviations the spread is away from its mean. Upper and lower thresholds are defined based on the mean and standard deviation of the z-scores. When the z-score exceeds the upper threshold, a short position is taken, indicating that the spread is likely to converge. Conversely, when the z-score falls below the lower threshold, a long position is taken.<br>

The strategy generates trading signals based on the z-score, and positions are established accordingly. The code calculates the number of shares to buy for each position based on an initial capital amount. The positions in the first and second assets are calculated separately.<br>

The code then constructs a portfolio to track the performance of the trading strategy. It includes columns for the asset prices, holdings in each asset, cash remaining after each trade, and the total value of each asset and the portfolio. The portfolio is updated based on the trading signals and positions.<br>

Finally, the code calculates the terminal wealth of the portfolio, representing the final value of the total assets after executing the trading strategy. The terminal wealth is recorded in the 'Terminal Wealth' column of the results DataFrame.<br>

Statistical arbitrage with cointegration aims to identify pairs of assets that have a long-term relationship and exploit the short-term price divergences between them. By taking advantage of the mean-reverting nature of the spread, the strategy generates trading signals and establishes positions to profit from the price convergence. The performance of the strategy is evaluated by calculating the terminal wealth achieved through the trading strategy for each asset pair.
