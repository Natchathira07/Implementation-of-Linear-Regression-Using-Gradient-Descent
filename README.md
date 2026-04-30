# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries

2.Initialize dataset (e.g., population vs profit) 

3.Initialize parameters: slope m and intercept b 

4.Choose learning rate α and number of iterations 

5.For each iteration

6.Predict values:​y=mx+b

7.Compute error 

8.Update parameters using gradient descent 

9.Repeat until convergence 

10.Plot the regression line
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: VD Natchathira
RegisterNumber:  212224230178
*/
import numpy as np
import matplotlib.pyplot as plt
X = np.array([1, 2, 3, 4, 5], dtype=float)
y = np.array([2, 4, 5, 4, 5], dtype=float)
m = 0  # slope
b = 0  # intercept
learning_rate = 0.01
epochs = 1000
n = len(X)
for i in range(epochs):
    y_pred = m * X + b
    dm = (-2/n) * np.sum(X * (y - y_pred))
    db = (-2/n) * np.sum(y - y_pred)
    m = m - learning_rate * dm
    b = b - learning_rate * db
print("Slope (m):", m)
print("Intercept (b):", b)
y_pred = m * X + b
plt.scatter(X, y, color='blue', label='Actual Data')
plt.plot(X, y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("y")
plt.legend()
plt.show()
```

## Output:
<img width="1092" height="978" alt="Screenshot 2026-04-30 143414" src="https://github.com/user-attachments/assets/548baf92-851d-4219-85a5-afd1d7a9b6ef" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
