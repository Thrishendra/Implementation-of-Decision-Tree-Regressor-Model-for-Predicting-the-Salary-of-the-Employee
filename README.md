# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee
## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values. 

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: T Thrishendra

RegisterNumber: 212223230227
```python
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
![Image-1](https://github.com/user-attachments/assets/47254328-0779-4d61-8b70-d08e98e434b3)

![Image-2](https://github.com/user-attachments/assets/60ec3aa1-093c-4c33-a7f3-878fe8a844eb)

![Image-3](https://github.com/user-attachments/assets/3231fb93-4a0c-4ace-8a4c-b58d90530ed3)

![Image-4](https://github.com/user-attachments/assets/07907a99-cf3e-41d5-96c8-c69cae62b34d)

![Image-5](https://github.com/user-attachments/assets/37ffcf59-ddfc-4bc6-8a57-107e1f3c6122)

![Image-6](https://github.com/user-attachments/assets/eca3c858-550b-419d-93f0-153153d73b7c)

![Image-7](https://github.com/user-attachments/assets/73f1dec6-4e91-4341-9abf-cb6a128307aa)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
