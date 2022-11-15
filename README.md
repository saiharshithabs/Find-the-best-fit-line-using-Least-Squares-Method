# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the needed packages 2.Assigning hours To X and Scores to Y 3.Plot the scatter plot 4.Use mse,rmse,mae formmula to find.

## Program:
```
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: B S SAIHARSHITHA
RegisterNumber:  212220040139

import pandas as pd
import numpy as np
dataset=pd.read_csv('/content/Placement_Data.csv')
print(dataset.iloc[3])

print(dataset.iloc[0:4])

print(dataset.iloc[:,1:3])

#implement a simple regression model for predicting the marks scored by students
import pandas as pd
import numpy as np
dataset=pd.read_csv('/content/student_scores.csv')

#implement a simple regression model for predicting the marks scored by students
#assigning hours to X& Scores to Y
X=dataset.iloc[:,:-1].values
Y=dataset.iloc[:,1].values
print(X)
print(Y)

from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)

from sklearn.linear_model import LinearRegression
reg=LinearRegression()
reg.fit(X_train,Y_train)

Y_pred=reg.predict(X_test)
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error,mean_squared_error

plt.scatter(X_train,Y_train,color="green")
plt.plot(X_train,reg.predict(X_train),color='red')
plt.title("Traning set (H vs S)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()

plt.scatter(X_test,Y_test,color="purple")
plt.plot(X_test,reg.predict(X_test),color="pink")
plt.title("Test set (H vs S)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()

mse=mean_squared_error(Y_test,Y_pred)
print("MES = ",mse)

mae=mean_absolute_error(Y_test,Y_pred)
print("MAE = ",mae)

rmse=np.sqrt(mse)
print("RMSE = ",rmse)

```

## Output:
![image](https://user-images.githubusercontent.com/94679395/195085655-8300c13c-e33c-4bac-a026-5d33096f8ef7.png)
![image](https://user-images.githubusercontent.com/94679395/195085750-4071308e-9e75-40cd-adc0-40544725499b.png)
![image](https://user-images.githubusercontent.com/94679395/195085807-a468d9b4-fe4d-4d20-8770-cf2216ba8b93.png)
![image](https://user-images.githubusercontent.com/94679395/195085844-6fca57c0-9ebc-4f7f-b602-7adba4e228ae.png)
![image](https://user-images.githubusercontent.com/94679395/195085931-9cbe2672-da09-439b-a432-48f57252c282.png)



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
