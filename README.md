# retail-trade-prediction

This repository shows the steps taken to perform a time series analysis of the "[St. Louis Fed Retail Trade](https://fred.stlouisfed.org/series/SMU53426604200000001)" data published on the Fed's website.  

The data and Jupyter Notebook have been added to the repo so that anyone can recreate the steps involved and add their own insights. 

## Use of:
* **Jupyter Notebook** 2023.03.0-daily+82.pro2
    * **Main Packages used:** pandas, numpy, statsmodels,
    matplotlib

# Overview
## Key Findings
* Using a SARIMA model, we make predictions for retail trade for the time period from 2022-02-01 to 2023-05-01. To evaluate the accuracy of the predictions, we  utilize the mean absolute percentage error (MAPE). 

### Seattle Tacoma Bellevue
* The MAPE value on the test set is calculated to be 2.6%. This indicates that, on average, the predicted  values deviate from the actual values by 2.6%. 
![alt text](https://github.com/monacosc1/retail-trade-prediction/blob/main/images/seattle_prediction.png) 

### Dallas Fort Worth Arlington
* Using the same methodology, the MAPE for Dallas-Fort Worth-Arlington is 1.82%.
![alt text](https://github.com/monacosc1/retail-trade-prediction/blob/main/images/dallas_prediction.png) 

## Model Coefficients
* The SARIMA order is (11, 2, 0)(0, 0, 1, 12). Based on this order, we examine the coefficients of our model. Upon analyzing the p-values, we observe that all of them are less than 0.01. This indicates that all the components of the model hold significant importance in predicting the time series.
![alt text](https://github.com/monacosc1/retail-trade-prediction/blob/main/images/seattle_model_summary.png) 

# Next Steps
* To enhance the predictive power of the algorithm, we can incorporate exogenous variables.
* Given the clear presence of seasonality in the data, an alternative approach to ARIMA and its variations is to employ a time series forecasting algorithm such as Fbprophet. Fbprophet is well-suited for handling seasonality and can potentially improve the accuracy of the predictions.
* Analyze the error plot derived from the predicted values. This allows us to examine whether the errors exhibit a random pattern or if there are any discernible patterns indicating that the model failed to capture certain aspects of the data.

