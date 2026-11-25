# Implementation of Multivariate Linear Regression
## Developed by: Magesh M
## Reg no: 26017516
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1:Import Pandas and the required module from Scikit-learn.
### Step2:Read the carsemission.csv dataset.
### Step3:Select Weight and Volume as independent variables.
### Step4:Select CO2 as the dependent variable.
### Step5:Create and train a Multivariate Linear Regression model.
## Step6:Display the regression coefficients and intercept.
### Step7:Predict the CO₂ emission for:
Weight = 3300
Volume = 1300
## Step8:Display the predicted CO₂ emission.
## Program:
```
#Developed by: Magesh M
#Reg no: 26017516
# Dataset Setup - Run this cell before starting the experiment
import pandas as pd
url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"
df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)
print("Dataset loaded successfully.")
```
```
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
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:
<img width="922" height="242" alt="image" src="https://github.com/user-attachments/assets/fadf092c-5005-45e6-a544-7c756393fdc5" />

<img width="774" height="337" alt="image" src="https://github.com/user-attachments/assets/3f58ad8e-1253-4e1e-9bce-e9c5a1fb1cb2" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
