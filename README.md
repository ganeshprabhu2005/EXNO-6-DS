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
NAME : GANESH PRABHU J
REG NO:212223220023

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```

<img width="1313" height="217" alt="Screenshot 2025-10-27 104024" src="https://github.com/user-attachments/assets/eda07ac8-d29d-42fb-bcd6-34c6e22a3f56" />

# 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="769" height="472" alt="Screenshot 2025-10-27 104031" src="https://github.com/user-attachments/assets/ed186e00-96c7-4c93-8ed8-0d4ac597c5b9" />


2.Multi Line Plot
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

<img width="729" height="475" alt="Screenshot 2025-10-27 104038" src="https://github.com/user-attachments/assets/c2aee27b-d520-4141-a6f6-6eed9334a29e" />


**TO VISUALIZE RELATIONSHIPS**

1.Bar Chart
```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```


<img width="903" height="500" alt="Screenshot 2025-10-27 104046" src="https://github.com/user-attachments/assets/e4627086-1181-416b-8776-370a7e576370" />


2.Scatter Plot
```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```


<img width="681" height="474" alt="Screenshot 2025-10-27 104053" src="https://github.com/user-attachments/assets/aa4694e3-c6b4-4182-b85e-396b8787a6d1" />


3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="844" height="474" alt="Screenshot 2025-10-27 104100" src="https://github.com/user-attachments/assets/c5a7dc94-f650-4c70-8957-9b50a49f0248" />



**TO CAPTURE DISTRIBUTIONS**

1.Histogram
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="759" height="476" alt="Screenshot 2025-10-27 104107" src="https://github.com/user-attachments/assets/5b4309bb-51f8-4947-b565-1258f36b5d04" />


2.Box Plot
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

<img width="771" height="479" alt="Screenshot 2025-10-27 104115" src="https://github.com/user-attachments/assets/14223f17-e1b5-423b-b930-af54ecff7465" />

3.Violin Plot
```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="816" height="473" alt="Screenshot 2025-10-27 104122" src="https://github.com/user-attachments/assets/b9657c08-1cb6-4384-be66-e8ed3ce7eb03" />


4.Density Plot
```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="798" height="488" alt="Screenshot 2025-10-27 104129" src="https://github.com/user-attachments/assets/15039c6e-f467-4472-b00a-9c58f6458b0d" />


5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="843" height="522" alt="Screenshot 2025-10-27 104136" src="https://github.com/user-attachments/assets/eee8cbba-f620-4136-8d2a-dac7916eba1d" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
