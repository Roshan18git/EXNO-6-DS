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
df=pd.read_csv("titanic_dataset.csv")
df.head()


```

<img width="1533" height="416" alt="image" src="https://github.com/user-attachments/assets/2c4bc6a5-4e99-4449-ade3-333e1f5dc546" />


```

1)LINE PLOT
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```

<img width="1147" height="687" alt="image" src="https://github.com/user-attachments/assets/3a82ea44-660e-4102-b4e5-eb9f1091d0e3" />

```

2)MULTI LINE PLOT

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')

```


<img width="1034" height="771" alt="image" src="https://github.com/user-attachments/assets/73757ba3-e0a4-437c-8cce-3836b0ae6692" />

```

TO VISUALIZE RELATIONSHIPS



1) Bar Chart

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="1638" height="719" alt="image" src="https://github.com/user-attachments/assets/1430cd82-0b51-42d5-aaa7-ece047ff86ed" />

```
2.Scatter Plot


sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```

<img width="1251" height="670" alt="image" src="https://github.com/user-attachments/assets/1549bde8-0b7c-470b-a5d4-7e70bc4ae315" />

```
3.Bubble Chart


sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```


<img width="1042" height="679" alt="image" src="https://github.com/user-attachments/assets/cc77aea2-4450-466f-822e-b93244f644de" />

```
TO CAPTURE DISTRIBUTIONS


1.Histogram

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```


<img width="1152" height="629" alt="image" src="https://github.com/user-attachments/assets/f2d5c3b8-5958-4342-8801-581985883e12" />

```

2.Box Plot


sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```


<img width="1664" height="772" alt="image" src="https://github.com/user-attachments/assets/39836f83-0156-4988-a110-0a8051d9a3d9" />

```

3.Violin Plot


sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="1391" height="683" alt="image" src="https://github.com/user-attachments/assets/86a1d73f-fd49-41e3-a731-ecef99d16426" />

```

4.Density Plot


sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```


<img width="1190" height="787" alt="image" src="https://github.com/user-attachments/assets/55af4816-b019-4006-8b7a-7670b72daba6" />

```

5.Heatmap


numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()


```


<img width="1079" height="742" alt="image" src="https://github.com/user-attachments/assets/58d23ecf-1fd2-4dd9-9ab3-33c62f489fea" />


# Result:

Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
