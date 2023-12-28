# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.Get the independent variable X and dependent variable Y.
2.Calculate the mean of the X -values and the mean of the Y -values.
3.Find the slope m of the line of best fit using the formula. eqn1
4.Compute the y -intercept of the line by using the formula: eqn2
5.Use the slope m and the y -intercept to form the equation of the line.
6.Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
# Program to find Multivariate Linear Regression
# Developed by : Hariharan A
# Reg no : 212223110013

import pandas as pd
from sklearn import linear_model
data=pd.read_csv("cars.csv")
x=data[["Weight","Volume"]]
y=data[["CO2"]]
regr=linear_model.LinearRegression()
regr.fit(x,y)
print("Coefficients:",regr.coef_)
print("Intercept:",regr.intercept_)
predictCO2=regr.predict([[3300,1300]])
print("predicted CO2 for the corresponding weight and volume", predictCO2)

```
## Output:
![Screenshot 2023-12-28 195536](https://github.com/hariharana59/Multivariate-Linear-Regression/assets/144980130/ec9bd1fd-ff39-45ba-83e5-2509c235f224)



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
