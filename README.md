# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score


## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MUGIL M.
RegisterNumber: 212223230127
```
```
import pandas as pd
data=pd.read_csv("/Salary.csv")
data.head()
data.info()
data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
![image](https://github.com/user-attachments/assets/a236d224-1edd-44f7-8bb7-174b5f9872d9)

![image](https://github.com/user-attachments/assets/94b59e82-6e8a-4c77-91d9-84c22e78c402)


![image](https://github.com/user-attachments/assets/9e689915-81dc-471b-bfb2-a3b8cf7807db)

![image](https://github.com/user-attachments/assets/b523ec58-5652-4465-a99f-e5215fc3895f)

![image](https://github.com/user-attachments/assets/61e73442-6f1c-486b-b8bd-12c8a87a8679)

![image](https://github.com/user-attachments/assets/ebb7dd36-224a-4864-a353-af213a024366)

![image](https://github.com/user-attachments/assets/c982ed7a-883f-4c24-a024-4ec80728aa8f)


![image](https://github.com/user-attachments/assets/ee1325a0-ffc8-4c86-8d2d-baf447081359)

![image](https://github.com/user-attachments/assets/d1e27212-2e4e-4afb-9ad2-c4dd0ceed108)


![image](https://github.com/user-attachments/assets/efb69d7d-962e-4a66-8d40-b9043f95164e)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
