# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary libraries.
2. Read and analyze the dataset
3. Preprocess the data
4. Define the input and output features
5. Split the data into training and testing data
6. Train the model using .fit() and predict using .predict()
7. Measure it's mse
8. Predict with a new data

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: RADHIMEENA M
RegisterNumber:  212223040159
*/
```


          import pandas as pd
          data=pd.read_csv('/content/Salary.csv')
          data.info()
          data.head()
          
          
          from sklearn.preprocessing import LabelEncoder
          le=LabelEncoder()
          data['Position']=le.fit_transform(data['Position'])
          
          
          x=data[['Position','Level']]
          y=data['Salary']
          
          
          from sklearn.model_selection import train_test_split
          x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
          
          
          from sklearn.tree import DecisionTreeRegressor
          dt=DecisionTreeRegressor()
          
          
          dt.fit(x_train,y_train)
          y_pred=dt.predict(x_test)
          
          
          from sklearn import metrics
          mse=metrics.mean_squared_error(y_test,y_pred)
          print(mse)
          
          dt.predict([[5,6]])

## Output:

![image](https://github.com/user-attachments/assets/c55374a9-65b8-4381-9c20-a6e14bd926ca)
![image](https://github.com/user-attachments/assets/227ed73b-8bc4-46ff-a2b6-69e67b57a08c)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
