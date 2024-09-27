## Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Jabez S
RegisterNumber: 212223040070
*/
import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])
```

## Output:
# data.head()
![Screenshot 2024-09-27 132241](https://github.com/user-attachments/assets/2fd88c88-a6d8-47bf-9345-3c39785c2640)
# data.info()
![Screenshot 2024-09-27 132333](https://github.com/user-attachments/assets/51e8bbb1-b787-47ab-8ffd-0eec7de42236)
# data.isnull().sum()
![Screenshot 2024-09-27 132344](https://github.com/user-attachments/assets/606dfa20-3c53-4e34-9dfd-4b8904f3dc4a)
# Position,Level,Salary
![Screenshot 2024-09-27 132355](https://github.com/user-attachments/assets/35a74b83-936c-451c-b602-bb15d1f7279f)
# 1
![Screenshot 2024-09-27 132408](https://github.com/user-attachments/assets/71a59f1e-155c-491b-a4bc-22be2cefea27)
# 2
![Screenshot 2024-09-27 132429](https://github.com/user-attachments/assets/2db5faff-c8c4-48db-b3cd-9737076cc510)
# 3
![Screenshot 2024-09-27 132445](https://github.com/user-attachments/assets/78573ad9-4cb1-4d5c-a5b7-8d9372f7229d)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
