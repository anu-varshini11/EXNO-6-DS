# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1609" height="262" alt="1" src="https://github.com/user-attachments/assets/135e9271-cd79-43be-a51f-620d13b5614f" />

### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/2b7fed29-04ac-42de-b325-5ad68b3e36b2" width="300" height="300"> 

### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="1026" height="580" alt="3" src="https://github.com/user-attachments/assets/e0e195ff-351c-44b3-a0d6-4711dfa84c52" />

## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1227" height="596" alt="4" src="https://github.com/user-attachments/assets/c545220d-c430-4579-95a5-1a13675d6f31" />



### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="1084" height="569" alt="5" src="https://github.com/user-attachments/assets/2a5ec018-327f-401a-a3d4-62d23d801fa3" />


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="1059" height="581" alt="6" src="https://github.com/user-attachments/assets/d588293c-666c-4a34-abbc-4cb02f1f68aa" />


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="1002" height="567" alt="7" src="https://github.com/user-attachments/assets/de47d157-bee5-4a90-a1ad-957a87948376" />

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="968" height="566" alt="8" src="https://github.com/user-attachments/assets/5f66136b-e250-4245-9e60-32e713140a27" />


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="1152" height="571" alt="9" src="https://github.com/user-attachments/assets/25ba505a-a815-4d3d-9b44-4329da4c26ee" />



### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="1118" height="559" alt="10" src="https://github.com/user-attachments/assets/7fe12e91-12d8-4787-8f72-35f2bd928525" />

### 5.Heatmap

```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1002" height="602" alt="11" src="https://github.com/user-attachments/assets/cb3b26cc-ab2a-49cb-b07e-669e28827015" />

## Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
