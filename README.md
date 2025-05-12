# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2.Import Decision tree regressor
3.Fit the data in the model
4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: M.Suryakumar
RegisterNumber:  212224040340
*/
import pandas as pd
df=pd.read_csv("/content/Salary.csv")
df.head()
df.info()
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()
x=df[['Position','Level']]
x.head()
y=df['Salary']
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![image](https://github.com/user-attachments/assets/d3db3387-863d-45a2-9e9d-551cf0eca818)
![image](https://github.com/user-attachments/assets/33a2d7fb-7459-4fb5-aa4f-853f7c5bc47a)
![image](https://github.com/user-attachments/assets/dc51416c-4408-4f57-830b-91b337c821fe)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
