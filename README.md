# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Start
Step 2: Import libraries

Import the required Python libraries:

numpy for numerical operations
matplotlib.pyplot for plotting graph
LinearRegression from sklearn.linear_model
Step 3: Define dataset

Create input and output data:

X=[1,2,3,4,5]
Y=[35,50,65,70,85]
Step 4: Reshape input

Convert X into a 2D array using reshape:

X=X.reshape(−1,1)
Step 5: Create model

Initialize Linear Regression model:

model = LinearRegression()
Step 6: Train model

Fit the model using data:

model.fit(X,Y)
Step 7: Get parameters

Extract:

Slope m
Intercept b
Step 8: Display equation values

Print:

Slope (m)
Intercept (b)
Step 9: Take user input

Input hours studied:

x_input
Step 10: Predict output

Use formula:

Y=mX+b

Predict marks using model.

Step 11: Display prediction

Print predicted marks.

Step 12: Plot graph
Scatter plot for actual data
Line plot for predicted regression line
Add labels and title
Step 13: Show graph
Step 14: Stop

## Program:
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression


X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()


model.fit(X, Y)


m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)


x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])


Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
![Uploading image.png…]()

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
