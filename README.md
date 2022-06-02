# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
```
NAME: RAKSHITHA DEVI J
REG NO: 212221230082
```
```
import pandas as pd
import numpy as np
df=open('Superstore.csv', encoding='windows-1252')
df = pd.read_csv("Superstore.csv",encoding='windows-1254')
df.head()
```
## DATA VISTUALISATION USING SEABORN:
```
import seaborn as sns
from matplotlib import pyplot as plt
plt.figure(figsize=(8,5))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
sns.violinplot(x="Profit",data=df)
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.pointplot(x=df["Quantity"],y=df["Discount"])
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
sns.kdeplot(x="Profit", data = df,hue='Categor
```

## Data Visualization Using MatPlotlib
```
plt.plot(df['Category'], df['Sales'])
plt.show()
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()
df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
plt.bar(df.index,df['Category'])
plt.show()
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
plt.boxplot(x="Sales",data=df)
plt.show()
```

# OUPUT

## DATA VISTUALISATION USING SEABORN:

![image](https://user-images.githubusercontent.com/94165326/171550808-2ccf9280-f264-4dda-8ef4-f2d10453715b.png)

![image](https://user-images.githubusercontent.com/94165326/171550823-d6d5c64b-26bd-4133-ba35-49cf7476c9f1.png)

![image](https://user-images.githubusercontent.com/94165326/171550845-fdc77183-700c-417a-b18f-d83313827989.png)

![image](https://user-images.githubusercontent.com/94165326/171550860-c4e67b79-9daf-49b6-84b5-14dd9b5a46d0.png)

![image](https://user-images.githubusercontent.com/94165326/171550879-6d327978-b7d5-49ee-b35f-ff5e88960b37.png)

![image](https://user-images.githubusercontent.com/94165326/171550912-95f0132f-1416-4db9-ad8e-a02c6053c3fa.png)

![image](https://user-images.githubusercontent.com/94165326/171550925-4eb8fa36-898a-4490-8eae-46f81537771d.png)

![image](https://user-images.githubusercontent.com/94165326/171550949-382ae564-6893-4cfb-b8e6-b178d79eb761.png)

![image](https://user-images.githubusercontent.com/94165326/171550965-da41b6f5-4109-4ae4-9fb4-7c3dab8fbdb6.png)

![image](https://user-images.githubusercontent.com/94165326/171550986-10ba6198-023b-4826-81e6-115ed33bb280.png)



## Data Visualization Using MatPlotlib

![image](https://user-images.githubusercontent.com/94165326/171551019-2174cd54-013c-4899-87a2-9c2c382ac2de.png)

![image](https://user-images.githubusercontent.com/94165326/171551048-419e2e19-c314-4026-8819-4c511d8639b5.png)

![image](https://user-images.githubusercontent.com/94165326/171551068-f1b02d50-d577-49d2-823a-616fa9b0b009.png)

![image](https://user-images.githubusercontent.com/94165326/171551085-6799dc72-5ff8-499b-b658-be963970677b.png)

![image](https://user-images.githubusercontent.com/94165326/171551105-2b4aaf5e-317a-4353-acda-357635908f2b.png)

![image](https://user-images.githubusercontent.com/94165326/171551123-373e8358-ae7d-44af-a2a5-58d2706fae26.png)

![image](https://user-images.githubusercontent.com/94165326/171551146-c3a7e244-9d6f-4b4f-ab05-0408c49fb878.png)

![image](https://user-images.githubusercontent.com/94165326/171551170-d867cee5-874b-48e9-b1f9-f08729489b21.png)


### RESULT:

Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.


