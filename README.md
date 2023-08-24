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
import numpy as np
import matplotlib.pyplot as plt

# Simulated data
X = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])  # Independent variable
Y = np.array([2, 4, 5, 4, 6, 7, 8, 8, 10, 9])  # Dependent variable

# Calculate means
x_mean = np.mean(X)
y_mean = np.mean(Y)

# Calculate slope (m) and y-intercept (b)
m = np.sum((X - x_mean) * (Y - y_mean)) / np.sum((X - x_mean)**2)
b = y_mean - m * x_mean

# Equation of the line
equation = f"Y = {m:.2f}X + {b:.2f}"

# Create the best fit line
best_fit_line = m * X + b

# Plotting the data points and the best fit line
plt.scatter(X, Y, label='Data Points')
plt.plot(X, best_fit_line, color='red', label='Best Fit Line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression')
plt.legend()
plt.grid(True)
plt.text(6, 9, equation, fontsize=12, color='blue')
plt.show()

```

## Output:
![Screenshot (18)](https://github.com/arun1111j/Find-the-best-fit-line-using-Least-Squares-Method/assets/128461833/41c290d7-918c-4d5d-b6b8-3494be1de6c3)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
