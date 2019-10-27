# Yellow Taxi Demand Prediction


  # Objectives & Constraints
## Objectives:
Our objective is to predict the number of pickups as accurately as possible for each region in a 10min interval. We will break up the whole New York City into regions, that we will discuss later in the blog. Now, the 10min interval is chosen because in NYC one can commute 1 mile in approximately 10 minutes given the traffic is normal at that particular time.
## Constraints:
**Latency:** Given a location and current time of a taxi driver, as a taxi driver, he/she excepts to get the predicted pickups in his/her region and the adjoining regions in few seconds. Hence, there is a medium latency requirement.

**Interpretability:** As long as taxi driver gets good prediction result, he/she is not be much interested in the interpretability of the result. He/she is not much interested in why he/she is getting this result. Hence, there is a no interpretability required.

**Relative Errors:** Mean Absolute Percentage Error will be the relative error we will consider. Let say the predicted pickups for a particular location are 100, but actual pickups are 102, the percentage error will be 2% and Absolute error is 2. The taxi driver will be more interested in the percentage error than the absolute error. Let say in some region the predicted pickups are 250, and if taxi driver knows that the relative error is 10% then he/she will consider the predicted result to be in the range of 225 to 275, which is considerable.

**Our goal is to reduce the percentage error as low as possible.**

## Steps -
Convert the given time series data into 10 minute interval bins.
Break the region of new york city into some clusters say k.
Group the time series data for each cluster.
Apply any feature engineering techniques to generate some more time series features.
Perform Train-Test Split.
Train Models.
Evaluate and Display MAPE in Tabular Format for all the models built.
## Conclusion -
**From the above result we have following observations:**
1. The difference between train error and test error of Random Forest Regressor is high, which clearly shows that Random Forest Regressor is overfitting. Therefore, we are discarding Random Forest Regressor.
2. The best model with lowest train and test MAPE error is XGBoost Regressor.
