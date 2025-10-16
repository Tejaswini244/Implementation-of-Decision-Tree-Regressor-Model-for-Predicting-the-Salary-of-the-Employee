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
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: R.TEJASWINI
RegisterNumber:212224230218  
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()

```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
R2 score:  0.48611111111111116


```
```
dt.predict([[5,6]])
```

## Output:
<img width="376" height="429" alt="Screenshot 2025-10-16 081609" src="https://github.com/user-attachments/assets/65f56847-9042-488f-85f0-36778bed8369" />



<img width="343" height="262" alt="Screenshot 2025-10-16 081622" src="https://github.com/user-attachments/assets/726b254f-747f-4a81-adfe-460b4c080b3e" />



<img width="160" height="297" alt="Screenshot 2025-10-16 081636" src="https://github.com/user-attachments/assets/2258d582-567b-4ace-8ccb-963c7e0090f4" />



<img width="316" height="36" alt="Screenshot 2025-10-16 082031" src="https://github.com/user-attachments/assets/db2f9014-7d78-4894-b9f1-12e6721f8c70" />



<img width="214" height="40" alt="Screenshot 2025-10-16 082040" src="https://github.com/user-attachments/assets/ff9bdd18-3aba-44cb-a5e4-644e92f1a58f" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
