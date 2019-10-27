# Yellow Taxi Demand Prediction

## Task -
Given previous info about number of pickups in regions, predict the expected number of pickups in the next 10 minute interval

## Steps -
Convert the given time series data into 10 minute interval bins.
Break the region of new york city into some clusters say k.
Group the time series data for each cluster.
Apply any feature engineering techniques to generate some more time series features.
Perform Train-Test Split.
Train Models.
Evaluate and Display MAPE in Tabular Format for all the models built.
## Conclusion -
XgBoost Had the least MAPE of around 10 %
Winter Holts Triple Exponential Features helped to achieve the results.
