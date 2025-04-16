# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary python libraries to perform the decision tree for regression problems.
2. Use pandas library of read.csv to read the csv file.
3. Use X as independent variable and y as dependent variable.
4. Use decision tree regressor to solve the regression problems
5. Use y_pred and use predict the future outcomes.
6. Print the predicted variable (y_pred).
7. Use sklearn.metrics to impore r2_score to get the performance score of the model.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: VESHWANTH.
RegisterNumber: 212224230300  
*/
import pandas as pd
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from sklearn.metrics import r2_score
data=pd.read_csv("C:\\Users\\admin\Downloads\\Salary.csv")
data.head()
data.info()
data.isnull().sum()
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
r2=r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
![1](https://github.com/user-attachments/assets/eeae90ba-6e39-4e5e-baea-841e9014e797)
![2](https://github.com/user-attachments/assets/afd3f573-fd7a-45da-824c-2e4b18603579)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
