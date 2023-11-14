# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm


1.Import the necessary python packages using import statements.


2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().


3.Split the dataset using train_test_split.


4.Calculate Y_Pred and accuracy.


5.Print all the outputs.


6.End the Program.



## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Vishwa vasu R
RegisterNumber: 212222040183

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

import chardet 
file='/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:



RESULT OUTPUT:



![Screenshot (101)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/84940cf8-821c-486c-98ae-b16b56a13265)




data.head():




![Screenshot (102)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/372f4fd2-df43-4c04-b8bf-9dfdf21a3784)






data.info():




![Screenshot (103)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/19150a29-bbb1-4fcb-8929-2d9d81372033)





data.isnull().sum():






![Screenshot (104)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/484bcdfc-f6f8-4beb-a24d-34337dc34766)






Y_prediction VALUE:






![Screenshot (106)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/9ceb3368-cb2f-4241-9051-d4dd267cffa7)







ACCURACY VALUE:







![Screenshot (107)](https://github.com/MaheshMuthuL/Implementation-of-SVM-For-Spam-Mail-Detection/assets/135570619/e5ade1dc-bf75-4bab-b17e-249250024c86)






## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
