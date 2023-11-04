# Ex:05 Feature Generation
## AIM :
To read the given data and perform Feature Generation process and save the data to a file.

## EXPLANATION :

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM :
STEP 1 :
Read the given Data

STEP 2 :
Clean the Data Set using Data Cleaning Process

STEP 3 :
Apply Feature Generation techniques to all the feature of the data set

STEP 4 :
Save the data to the file

## PROGRAM :
```
JENISHA.J
212222230056
```
#### bmi.csv
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2

```

#### data.csv
```
import pandas as pd
df1 = pd.read_csv("/content/data (1).csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```

#### Encoding.csv
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data (1).csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
## OUTPUT :
#### bmi.csv
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/f1cd6d14-34f5-4379-8c57-6d333c313f2d)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/e28c999d-3891-481c-98ee-94dd1daa0c9e)

#### data.csv
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/4e038c71-dd2c-46b5-8e73-4ac9348e61ef)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/a771f8e6-7af6-4076-82a7-85c66e302463)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/a8a8aaef-50e8-4640-adb3-64b040082117)

#### Encoding.csv
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/1e868405-bcd8-4d14-874c-568446e501a0)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/a9848ba0-717a-47b9-8e55-10d5885442e8)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-05/assets/119405070/821590b7-a94e-4f2d-b432-97bc9d3e0c79)

## RESULT:
The Feature Generation process was performed and saved the data to a file.
