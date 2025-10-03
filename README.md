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
Developed by: Titus Ratna Kumar Karivella 
RegisterNumber:  212224230292
```

```py
import pandas as pd
data=pd.read_csv("Salary.csv")
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
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)

dt.predict([[5,6]])
```

## Output:

<img width="958" height="299" alt="image" src="https://github.com/user-attachments/assets/f15b4319-1aad-4897-bb53-caab0bb83220" />


<img width="399" height="195" alt="image" src="https://github.com/user-attachments/assets/61dd25b1-4788-4f8f-8054-df5dba7f1980" />

<img width="697" height="131" alt="image" src="https://github.com/user-attachments/assets/f8326bb9-1e78-436c-9eeb-d3623c597da9" />

<img width="323" height="35" alt="image" src="https://github.com/user-attachments/assets/95fe22c5-f51a-4c1f-8d93-d26593d43a95" />

<img width="200" height="35" alt="image" src="https://github.com/user-attachments/assets/efa1ff34-c6c2-4970-b24b-be09127c646c" />






## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
