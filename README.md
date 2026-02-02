# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: F.Senash Ayisha
RegisterNumber: 25018487

import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5, 6, 7])       #data
y = np.array([45, 50, 55, 60, 62, 68, 72])

x_mean=np.mean(x)      #mean
y_mean=np.mean(y)

n=0  #numerator and denominator
d=0
for i in range(len(x)):
    n=n+(x[i]-x_mean) * (y[i]-y_mean) 
    d=d+((x[i] - x_mean) ** 2)
    m=n/d        #slope

b=y_mean - m*x_mean     # intercept
print("intercept=",b)
print("slope=",m)

y_predict=m*x +b         #prediction
print("y_predict=",y_predict)

plt.scatter(x,y)         #plot
plt.plot(x,y_predict,color="red")
plt.grid(True)
plt.xlabel("Actual x value")
plt.ylabel("Predicted y value")
plt.legend("Actual x vs Predicted y")
plt.show()
    
    
*/
```

## Output:
<img width="1006" height="713" alt="image" src="https://github.com/user-attachments/assets/671947a7-cdbe-466b-85fe-207f793d79cc" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
