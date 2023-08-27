# student-dropout-prediction

This repository shows the steps taken to perform a classification analysis of the "[Student Outcomes in Higher Education](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)" data published on the the UC Irvine Machine Learning Repository.  

The data and Jupyter Notebook have been added to the repo so that anyone can recreate the steps involved and add their own insights. 

## Use of:
* **Jupyter Notebook** 2023.03.0-daily+82.pro2
    * **Main Packages used:** pandas, numpy, statsmodels,
    matplotlib, catboost, imlearn

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
* The final classification model had a validation accuracy of 89%.
![alt text](https://github.com/monacosc1/retail-trade-prediction/blob/main/images/seattle_model_summary.png) 

# Next Steps
* Feature selection methods like backward elimination can be used to choose the most relevant features.
* To handle class imbalance, more sophisticated techniques such as resampling methods (e.g., SMOTE) or ensemble methods (e.g., Random Forest, Gradient Boosting) can be employed.
* Instead of using the Min-Max scaler, considering Mean-Variance scaling (StandardScaler) might be a better choice
* Ensemble methods, like a stacked approach to classification (Stacking), can be utilized to combine multiple classifiers, potentially leading to improved predictive performance by leveraging the strengths of each model in the ensemble.

