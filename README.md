# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step 1: import pandas as pd.

Step 2: Read the csv file.

Step 3: Get the value of X and y variables.

Step 4: Create the linear regression model and fit.

Step 5: Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube.

Step 6: Print the predicted output.

## Program:
```
#Developed By: S.NAVINKUMAR
#Register no : 212224110041

import pandas as pd
from sklearn import linear_model
data = {
    'Weight': [1000,1200,1000,900,1500,1000,1400,1500,1500,1600,1100,1300,1000,1600,1600,1600,1600,2200,1600,2000,1600,2000,2100,1600,2000,1500,2000,2000,600,2000,2100,2000,1600,1600,1600,2500],
    'Volume': [790,1160,929,865,1140,929,1109,1365,1112,1150,980,990,1112,1252,1326,1330,1365,1280,1119,1328,1584,1428,1365,1415,1415,1465,1490,1725,1523,1705,1605,1746,1235,1390,1405,1395],
    'CO2': [99,95,95,90,105,105,90,92,98,99,99,101,99,94,97,97,99,104,104,105,94,99,99,99,99,102,104,114,109,114,115,117,104,108,109,120]
}
df = pd.DataFrame(data)
df.to_csv("car.csv", index=False)
df = pd.read_csv("car.csv")
X = df[['Weight', 'Volume']]
Y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, Y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3000], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
<img width="1517" height="499" alt="image" src="https://github.com/user-attachments/assets/837e00cb-832a-4bca-9392-3b2565c1b59e" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
