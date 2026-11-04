# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br> Import the required libraries such as NumPy, Pandas and Linear Regression from Scikit-learn.

### Step2
<br> Create a dataset containing multiple independent variables (hours studied, hours slept and attendance) and one dependent variable (marks).

### Step3
<br> Separate the independent variables (X) and dependent variable (Y).

### Step4
<br> Create and train the Multivariate Linear Regression model using the fit() function.

### Step5
<br> Predict the output for new input values using the predict() function and display the predicted result.

## Program:


### Dataset Setup - Run this cell before starting the experiment

```
import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("car (1).csv", index=False)
print("Dataset loaded successfully.")

```
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car (1).csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
```
Coefficients: [0.00755095 0.00780526]
Intercept: 79.69471929115939
Predicted CO2 for the corresponding weight and volume: [114.75968007]
```

### Insert your output

<br>
<img width="1663" height="772" alt="image" src="https://github.com/user-attachments/assets/f399728a-a68c-44c1-837a-f373f0d26eeb" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
