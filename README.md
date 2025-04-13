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
![image](https://github.com/user-attachments/assets/033a31a8-9289-4d8b-b69a-2b20bb1390ef)

```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/f129854e-39ca-4909-ba58-3d41d603a482)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto",palette="Set1")
```
![image](https://github.com/user-attachments/assets/fed1647d-de6b-41a8-b8c9-c0573506e0fd)

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
![image](https://github.com/user-attachments/assets/ae3edf58-dde0-4fac-b2cd-13d84cc88b6e)

```

tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/dc1d8233-0c68-4fb9-aebb-d72624b43ac5)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill",width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```
![image](https://github.com/user-attachments/assets/8157b2a4-2628-46e4-ba56-5d72102021d9)

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
![image](https://github.com/user-attachments/assets/976b56bd-e995-4c88-a83a-d434b2b2d55b)

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df,palette="Set1")
plt.xlabel("Totsl Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```
![image](https://github.com/user-attachments/assets/95e75c55-55df-44ca-9170-48dc8719098e)
```
sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
![image](https://github.com/user-attachments/assets/001b00fb-afb3-42a8-8385-fa5ec36e3f3f)

```
import seaborn as sns
import pandas as pd
df=sns.load_dataset('tips')
sns.boxplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
```
![image](https://github.com/user-attachments/assets/6e31d44d-7383-43ab-b25e-d8c7d541e260)

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette='Set1')
```
![image](https://github.com/user-attachments/assets/9ec22792-014c-413e-af69-c548e7b9c15f)

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette='Set1',inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/9b2d9443-4f01-4372-83e2-25b7afc7b09b)

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip,palette="Set2")
```
![image](https://github.com/user-attachments/assets/1a06bdc4-a82a-4214-8e3c-4e57d3d49fbe)

```
import seaborn as sns
sns.set(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"],palette="Set1")
```
![image](https://github.com/user-attachments/assets/e01fae7a-727c-4d4a-af5f-04425371ed83)

```
import seaborn as sns
sns.set(style="whitegrid")
tips = sns.load_dataset("tips")
sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")
```
![image](https://github.com/user-attachments/assets/a25660a9-0e9a-4118-8d0b-7b74df58c554)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette='Set2',alpha=0.8)

```
![image](https://github.com/user-attachments/assets/82cd630e-3b8c-4f59-a284-218e52756795)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set3',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/9cb67675-dccc-49af-9e91-29cf9752ac87)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set1',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/b2e415ef-5ae6-480c-a3d7-0b51734373cb)

```
import seaborn as sns
tip = sns.load_dataset('tips')
num=tips.select_dtypes(include=['float64','int64']).columns
corr = tips[num].corr()
sns.heatmap(corr,annot=True,cmap="YlGnBu")
```
![image](https://github.com/user-attachments/assets/a33f59f8-9fe3-4a24-96e4-e28bbe3ce737)

```
sns.heatmap(corr,cmap="YlGnBu")

```
![image](https://github.com/user-attachments/assets/6716405d-f818-448a-986b-a6bc47b72ae3)


# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
