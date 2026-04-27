# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2.Calculate the mean of the X -values and the mean of the Y -values.
3.Find the slope m of the line of best fit using the formula.
<img width="314" height="135" alt="Screenshot 2026-04-27 092214" src="https://github.com/user-attachments/assets/f1f8e6a7-436e-4f6c-a7d7-5680916f315c" />

4. Compute the y -intercept of the line by using the formula:
 <img width="222" height="47" alt="Screenshot 2026-04-27 092221" src="https://github.com/user-attachments/assets/8d2eb330-32e8-4e82-9331-a3a61c3840eb" />
 

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.


## Program:
```
/*
Developed by: MANOSHREE N
RegisterNumber:212225040228
# Step 1: Import Libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# Step 2: Create Dataset
data = {
    "Hours_Studied": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    "Marks_Scored":  [35, 40, 50, 55, 60, 65, 70, 80, 85, 95]
}
df = pd.DataFrame(data)

print("Dataset:\n", df)

# Step 3: Define Features and Target
X = df[["Hours_Studied"]]
y = df["Marks_Scored"]

# Step 4: Split Dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Step 5: Train Model
model = LinearRegression()
model.fit(X_train, y_train)

# Step 6: Predict
y_pred = model.predict(X_test)

# Step 7: Evaluation
print("\nModel Parameters:")
print("Intercept (b0):", model.intercept_)
print("Slope (b1):", model.coef_[0])

print("\nEvaluation Metrics:")
print("Mean Squared Error:", mean_squared_error(y_test, y_pred))
print("R2 Score:", r2_score(y_test, y_pred))

# Step 8: Visualization
plt.figure(figsize=(8,6))
plt.scatter(X, y, label="Actual Data")
plt.plot(X, model.predict(X), label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression")
plt.legend()
plt.grid(True)
plt.show()

# Step 9: Prediction for New Input
hours = 7.5
predicted_marks = model.predict([[hours]])
print(f"\nPredicted marks for {hours} hours = {predicted_marks[0]:.2f}")
*/
```

## Output:
<img width="415" height="274" alt="Screenshot 2026-04-27 091818" src="https://github.com/user-attachments/assets/ec1e65f0-82bd-4a64-9295-0a28cca7d8f1" />
<img width="927" height="782" alt="Screenshot 2026-04-27 091845" src="https://github.com/user-attachments/assets/5876bad0-b60e-4cdd-b3e4-00dd40c56532" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
