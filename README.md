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
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("C:/Users/admin/Downloads/titanic_dataset.csv")
print(df)
```
<img width="1441" height="177" alt="image" src="https://github.com/user-attachments/assets/09809eaf-abb4-462d-991e-097660e6c021" />
<img width="1435" height="910" alt="image" src="https://github.com/user-attachments/assets/7885b749-05fb-43fb-92dc-e86317d38a7d" />

df.head()
<img width="1451" height="296" alt="image" src="https://github.com/user-attachments/assets/1e2459f4-9c4e-4c59-985b-7432c8c950f3" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="1441" height="722" alt="image" src="https://github.com/user-attachments/assets/1cae9179-3a2d-40bf-8f91-beba13b5da9d" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="1435" height="819" alt="image" src="https://github.com/user-attachments/assets/3ea29b5c-f4b1-4a37-abe8-28894aada0f5" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1444" height="755" alt="image" src="https://github.com/user-attachments/assets/81d253c4-89de-4e1e-aaa5-7919e2101e9b" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="1438" height="698" alt="image" src="https://github.com/user-attachments/assets/122f8656-acf2-4509-b1c7-0e0d0859a7a4" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="1444" height="706" alt="image" src="https://github.com/user-attachments/assets/f8e7866f-81dd-4b74-8268-7b120c1275ff" />

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

<img width="1435" height="674" alt="image" src="https://github.com/user-attachments/assets/95bc2551-a240-4778-95c3-2ac6417c5b72" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1444" height="719" alt="image" src="https://github.com/user-attachments/assets/af4aabaf-b81d-4558-b7b5-b6f1145a4527" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="1435" height="702" alt="image" src="https://github.com/user-attachments/assets/2983daad-fd53-4181-9aa1-2f98ed4794d2" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="1441" height="843" alt="image" src="https://github.com/user-attachments/assets/44c1a6a4-08dc-468b-bfd7-3b1356ce04f7" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1448" height="803" alt="image" src="https://github.com/user-attachments/assets/62bc5698-beca-4280-9873-72b8a27d2ae0" />

# Result:

Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
