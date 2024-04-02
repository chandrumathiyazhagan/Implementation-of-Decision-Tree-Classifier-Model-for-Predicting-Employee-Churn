# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:

/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: 
RegisterNumber:  
*/
```python
import pandas as pd
data=pd.read_csv("/content/Employee_EX6.csv")
data.head()
```
```python
data.info()
```
```python
data.isnull().sum(
```
```python
data["left"].value_counts()
```
```python
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```python
data["salary"]=le.fit_transform(data["salary"])
data.head()
```
```python
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours",
                  "time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
```
```python
y=data["left"]
```
```python
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```
```python
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
```python
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
```python
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

![Screenshot 2024-04-02 160839](https://github.com/chandrumathiyazhagan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119393023/9271c57e-b3ab-4e0c-b57d-60b46602f8e2)

![Screenshot 2024-04-02 160852](https://github.com/chandrumathiyazhagan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119393023/c7942d5d-ebc7-4960-ac98-8d233396260d)

![Screenshot 2024-04-02 160907](https://github.com/chandrumathiyazhagan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119393023/16f67c00-7ad7-43d5-8467-cceddfdc73f3)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
