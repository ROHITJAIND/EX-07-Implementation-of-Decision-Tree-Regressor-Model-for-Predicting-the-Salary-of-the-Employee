# EX-07 Implementation of Decision Tree Regressor Model for Predicting the Salary of the Employee
### Aim:
To write a program to implement the Decision Tree Regressor Model &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE :**<BR>
for Predicting the Salary of the Employee.
### Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook
### Algorithm
1. Import pandas and read the csv file.
2. Encoding the data and Import Decision tree classifier.
3. Fit the data in the model.
4. Find the MSE , r2 and the Predicted.
### Program:
```Python
import pandas as pd
df=pd.read_csv("CSVs/Salary.csv")
df.head(10)
df.info()
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df['Position']=le.fit_transform(df['Position'])
df.head(10)
x=df[['Position','Level']]
y=df['Salary']
from sklearn.model_selection import train_test_split as tts
Xtrain,Xtest,Ytrain,Ytest=tts(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(Xtrain,Ytrain)
Ypred=dt.predict(Xtest)
from sklearn import metrics
mse=metrics.mean_squared_error(Ytest,Ypred)
mse
r2=metrics.r2_score(Ytest,Ypred)
r2
dt.predict([[5,6]])
```

**Developed By: ROHIT JAIN D** <BR>
**Register No : 212222230120** <BR>

### Output:
**df.head()**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**df.info()**<br>
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/3e26416c-15dd-438e-b94b-82fe6062d7ec">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/bc166b21-ba12-483f-86a9-87f78a11a444">
<br>
<br>
**df.isnull.sum()**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**After Label Encoding**<br>
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/a87bd2d8-ce65-4bda-b504-51a6e0a86754">  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/06f6314d-455a-4866-8e49-667f1f6830c9">
<br>
<br>
<BR>
<BR>
**MSE :**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; **r2 :**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**Predicted Value :**<br>
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/71de2a7a-ed0c-4b89-aee3-a71e7e82cec9">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/d5eab5c9-e084-40f3-8294-8be3989aaf5f">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
<img valign=top src="https://github.com/ROHITJAIND/EX-07-Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707073/43608200-8699-4611-9ad1-fea20a2e4840">






### Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
