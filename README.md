# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/a4f7e4ae-c677-4481-b3c8-99ac821ba23f)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/222551fe-210d-43ec-8005-698d8808e7a3)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/fe5a894a-171e-4093-8230-6fbaa745286d)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/9865dd51-771a-49fa-bd6d-6ecaf27e4587)

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/f9ad3a28-39fd-4ac9-b375-6114791157c1)


```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/23f9555c-3edd-4fdb-9cad-94106359e4e5)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/38a01607-59a6-46bf-9b1b-9f6efe891a2b)


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/b65ceba3-073f-4985-9320-4188130e5442)


```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/c5585334-ed70-4dbd-aba4-da6bad5e1932)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/3b8ba08d-30a6-4477-a1e5-c5b741b1976c)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/c5f43075-4f24-4804-8821-31b188fe65f9)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/8cde9c2d-4550-488d-86b6-e219600186f0)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/1be884f1-0d8a-45d2-a73b-a8f22c5a9109)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/b13d8ecc-63d8-4b83-b742-3213f1773925)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/54c97eb6-4e4e-4640-a276-fef352cd3e05)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/cde984e2-0fc1-46f7-9331-e159c5b56b1a)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/c1124f14-a9a1-4515-988b-d0aba9bd89ba)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/35e99d1b-2e58-4913-a459-e7a56c59fc09)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/eb4e0b83-2a78-44d2-9626-b5f10ebad9bd)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/302fb15f-dcda-4de5-8b65-a9be59134ce7)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/2b18f064-0a96-4874-9dfd-12c718541243)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/66909d83-9fd3-404f-9211-d46182dc9414)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/3dd3c8a1-156e-47f0-b24c-ef4c1498c839)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/60ffbeeb-b75c-419f-a082-44ec2b559bb1)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/ef01fc11-9ecd-4c54-8ecb-6c849f484194)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/389299bd-3f6c-4ab3-8ddd-fea0e9d47f99)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/lokeshnarayanan/EXNO-6-DS/assets/119393019/2a870a25-f226-4f16-9ed9-0453485a5bd8)

# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
