# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the packages.
2. Analyse the data.
3. Use modelselection and Countvectorizer to preditct the values.
4. Find the accuracy and display the result.

## Program:

/*

Program to implement the SVM For Spam Mail Detection..

Developed by: vishwa vasu R
 
RegisterNumber: 212222040183

*/

```
import chardet
file = "/content/spam.csv"
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
print(result)

import pandas as pd
data = pd.read_csv("/content/spam.csv", encoding='windows-1252')
print(data.head())

print(data.info())

print(data.isnull().sum())

x = data["v1"].values
y = data["v2"].values

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC
svc = SVC()
svc.fit(x_train, y_train)
y_pred = svc.predict(x_test)
print(y_pred)

from sklearn import metrics
accuracy = metrics.accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

```

## Output:

![image](https://github.com/user-attachments/assets/451f3bae-e9f3-4de0-b4d0-dea8e9ec8c6d)

![image](https://github.com/user-attachments/assets/3eb0b426-236e-48ed-9d2a-8c7e90c2825a)

![image](https://github.com/user-attachments/assets/d7d687c8-75a1-4c5c-b701-96b663fed84e)

![image](https://github.com/user-attachments/assets/32b9cb36-658b-4dbf-a0fd-9accde84fe45)

![image](https://github.com/user-attachments/assets/8c594fbe-c343-41db-a030-0ac8a5491adc)

![image](https://github.com/user-attachments/assets/7be7ece2-d1da-4330-adf3-2e76b9e2d71d)















## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
