63# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. Find the accuracy of the model and predict the required values by importing the required module from sklearn

## Program:
```

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PALADUGU VENKATA BALAJI
RegisterNumber:  2305001024


import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/374fc8f0-0f17-4117-a058-57a9c19fca43)
![image](https://github.com/user-attachments/assets/d3dbffd2-5764-438a-ad50-ffc781d4d2b1)
![image](https://github.com/user-attachments/assets/0ab94cce-55ba-4fc0-add5-8644db218dd6)
![image](https://github.com/user-attachments/assets/03fa54b0-3704-4ed1-b61a-845a54edb923)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
