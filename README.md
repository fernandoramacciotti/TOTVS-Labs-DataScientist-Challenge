# TOTVSLabs Data Challenge for Data Scientist position
### Fernando Martinelli Ramacciotti | fernandoramacciotti@gmail.com

Give a dataset of restaurant receipts, the objective of the challenge is:
1. Parse and extract the data.
2. Identify a pattern on any set of fields that can help predict how much a customer will spend.
3. Calculate a sales forecast for the next week.

In the notebook data_challenge you can find the full analysis done. The sales forecast for the next week is **$ 34,202.96**

Since the dataset is very small, a sophisticated forecast model cannot be applied due to weak statistical power. Therefore, the final sales forecast for the next week was calculated averaging three models:
1. Historical mean
2. Historical median
3. Facebook's prophet package for automatic time series forecasting.

A holdout period of 2 days was used to validate the model, using Mean Squared Error (MSE). The average of the three forecasts was weighted by the inverse of validation MSE of each model.

