# Quant Research Assignment

**Research Thesis**

Nifty and Bank Nifty indices have significant overlap in terms of their constituents and weights. Our thesis is that their volatilities are also likely to be affected by similar market conditions and macroeconomic factors. We can thus construct a pairs trading strategy that attempts to capture any dispersion that may occur between the volatilities of the two indices

This assignment will involve building a pairs trading strategy to test this hypothesis. The output we are looking for is a medium-frequency strategy that has a trading horizon ranging between 30 min to 5 days. 

**Dataset**

[data.parquet](Quant%20Research%20Assignment%208ac8c4464fd44c2988addaff28e18631/data.parquet)

1. Time series of minute-level implied volatilities (IVs) of Bank Nifty and Nifty.
2. Time To Expiry (TTE) for the series.
3. Indian market trading hours are between 09:15 and 15:30. 
4. There may be some missing values in the dataset.
5. The formula to calculate P/L has been specified below. If you modify your IV or spread series, make sure you modify the P/L equation as well.

**Deliverables**

1. Build a [z-score based](https://en.wikipedia.org/wiki/Standard_score) trading system. It would use the z-scores of the spread to identify when volatility has diverged away from the historical mean and act accordingly. The calculation of the P/L here constitutes the base model.
2. Build a better model than the z-score trading system. Be creative in the modeling techniques you implement.
3. Compare your proposed model with the base model to optimize the absolute P/L, Sharpe Ratio, and Drawdown of your strategy.

**Formulae**  

$$
\text{Spread} = \text{Bank Nifty IV} - \text{Nifty IV}

$$

$$
\text{P/L} = \text{Spread} \times (\text{Time To Expiry})^{0.7}

$$
