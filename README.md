# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Load and prepare data – read carsemission.csv into a DataFrame, then split it into feature variables (Weight, Volume) and the target variable (CO2).

### Step2
Instantiate the model – create a LinearRegression object from sklearn.
### Step3
Train (fit) the model – feed the feature matrix X and target y to regr.fit() so the algorithm learns the optimal coefficients and intercept.

### Step4
Inspect the learned parameters – output the model’s coefficients and intercept to understand how weight and volume influence CO₂ emissions.

### Step5
Make a prediction – build a one-row DataFrame with a new car’s weight and volume, pass it to regr.predict(), and print the estimated CO₂ emission for those inputs.

## Program:
```
Developed by : Abishek P
Register Number : 212224240002

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:',predictedCO2)
```
## Output:
## Coefficient and Intercept:
![image](https://github.com/user-attachments/assets/f388adb0-4f89-46b0-a8ab-5534afe76310)
## Predicted Co2:
![image](https://github.com/user-attachments/assets/0128f278-62e5-441e-8533-dc7dd3ad14e0)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
