# student-dropout-prediction

This repository shows the steps taken to perform a classification analysis of the "[Student Outcomes in Higher Education](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)" data published on the the UC Irvine Machine Learning Repository.  

The data and Jupyter Notebook have been added to the repo so that anyone can recreate the steps involved and add their own insights. 

## Use of:
* **Jupyter Notebook** 2023.03.0-daily+82.pro2
    * **Main Packages used:** pandas, numpy, statsmodels,
    matplotlib, catboost, imlearn

# Overview
## Key Findings
* Given an imbalanced dataset, we used a SMOTE method to balance both classes of "dropout" and "graduate".

### Marital Status by Target
* Legally Separated students are likely to drop out. By contrast, widowers are likely to graduate.
![alt text](https://github.com/monacosc1/student-dropout/blob/master/images/marital_status_by_target.png) 

### Mother's Occupation
* Students whose mothers are teachers, personal service, or professional service workers are likely to graduate.
![alt text](https://github.com/monacosc1/student-dropout/blob/master/images/mothers_occupation_by_target.png) 

### Area of Study
* Nursing and Social Science students are likely to graduate.
![alt text](https://github.com/monacosc1/student-dropout/blob/master/images/course_by_target.png) 

## Model Coefficients
* The final classification model had a validation accuracy of 89%.
![alt text](https://github.com/monacosc1/student-dropout/blob/master/images/accuracy_report.png) 

# Next Steps
* Feature selection methods like backward elimination can be used to choose the most relevant features.
* To handle class imbalance, more sophisticated techniques such as resampling methods (e.g., SMOTE) or ensemble methods (e.g., Random Forest, Gradient Boosting) can be employed.
* Instead of using the Min-Max scaler, considering Mean-Variance scaling (StandardScaler) might be a better choice
* Ensemble methods, like a stacked approach to classification (Stacking), can be utilized to combine multiple classifiers, potentially leading to improved predictive performance by leveraging the strengths of each model in the ensemble.

