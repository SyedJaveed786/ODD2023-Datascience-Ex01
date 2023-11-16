# Ex NO : 01   Data Cleansing

## DATE : 24/08/2023

## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

## Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

## ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

## CODE:
DEVELPOED BY : SYED JAVEED H

REGISTER NO : 212221220055
```
DATA CLEANING HANDLING NULL VALUES

import pandas as pd

df=pd.read_csv('/content/SAMPLEDS.csv')

df

df.shape

df.describe()

df.isnull().sum()

df.dropna(how='any').shape

x=df.dropna(how='any')

x

df.dropna(how='all').shape

tot = df.dropna(subset=['TOTAL'],how='any')

tot

m = df.dropna(subset=['M4'],how='any')

m

tot = df.dropna(subset=['M1','M2','M3','M4'],how='any')

tot

df.fillna(0)

df

df.fillna(method='ffill')

df.fillna(method='bfill')

mn=df.TOTAL.mean()

mn

df.TOTAL.fillna(mn,inplace=True)

df

l=df.M1.interpolate()

l

df.M1.fillna(l,inplace=True)

df

mn=df.TOTAL.median()

mn

df.TOTAL.fillna(mn,inplace=True)

df

l=df.M1.interpolate()

l

df.M1.fillna(l,inplace=True)

df

mn=df.TOTAL.mode()

mn

df.drop_duplicates(inplace=True)

df

df['cd']=pd.to_datetime(df['DOB'])

df

for x in df.index: if df.loc[x,"AVG"]>100: df.drop(x,inplace=True)

df
```
## OUTPUT:

![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/e1d0289d-2a36-4a14-b5a3-6145a15f3769)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/6cd0b29e-a964-432e-b2b2-77b2dfeef130)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/171d21b3-0847-4faf-948d-acf963038849)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/67953762-3357-4786-aa3e-4fce64f84493)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/99676258-a9a4-4217-8786-0ae04c44a0ef)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/5326e6ac-cc40-45ff-87dd-03da25da99a8)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/92008f1d-6567-4549-a939-5ff7bd459c10)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/d1d6fc27-b0ab-4fa5-8eb3-d8469ff522db)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/4c0f6822-476d-44c2-a139-54d1f06cb881)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/6ab7c00a-4997-4fbd-a1f5-4104d2ffb5b4)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/ff8fef88-7b9b-40aa-a3e5-46fe2c180447)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/c349aecd-a43c-46b8-aee5-4c006a48660e)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/0bfa1b90-5f6c-4edd-b35d-efb0fd1d74bf)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/24594b42-6a06-40bb-975a-53ead2946e1c)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/8c9b668e-52bc-412e-8373-39927e910312)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/89d1aeea-8ce0-478d-9d6e-37da80c6780d)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/e6784814-c9db-4c1a-85d0-355d33191203)
![image](https://github.com/SyedJaveed786/ODD2023-Datascience-Ex01/assets/106874713/2b8589ca-53a6-495d-ab30-286f95e97675)

## RESULT:

Thus,the given data is cleansed and the cleaned data is saved into the file.



















