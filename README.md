# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
/* 
Name : santhosh j
Register Number : 2122200220040
**Data Cleaning - Data_set.csv**
import numpy as np
import pandas as pd
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

**Data Cleannig - Loan_data.csv**
data = pd.read_csv("/content/Loan_data.csv")
print(data)
data.head(5)
data.isnull()
data.isnull().sum()
data['Gender'] = data["Gender"].fillna(data['Gender'].mode()[0])
data['Dependents'] = data["Dependents"].fillna(data['Dependents'].mode()[0])
data['Self_Employed'] = data["Self_Employed"].fillna(data['Self_Employed'].mode()[0])
data['Credit_History'] = data["Credit_History"].fillna(data['Credit_History'].mode()[0])
data.head()
data['LoanAmount']=data['LoanAmount'].fillna(data['LoanAmount'].median())
data.head()
data['Loan_Amount_Term']=data['Loan_Amount_Term'].fillna(data['Loan_Amount_Term'].mean())
data.head()
data.info()
data.isnull().sum()
*/
```
# OUPUT
## Data Cleaning - Data_set.csv
![Data Cleaning](/images/img.png)

## Before Cleaning
![Data Cleaning](/images/img2.png)
![Data Cleaning](/images/img3.png)

## Mode
![Data Cleaning](/images/mode.png)

## Mean
![Data Cleaning](/images/mean.png)

## Median
![Data Cleaning](/images/median.png)

## After Cleaning
![Data Cleaning](/images/img4.png)

## Data Cleaning - Loan_data.csv
![Data Cleaning](/images/image1.png)

## Before Cleaning
![Data Cleaning](/images/image2.png)
![Data Cleaning](/images/image3.png)

## Mode
![Data Cleaning](/images/mode2.png)

## Mean
![Data Cleaning](/images/mean2.png)

## Median
![Data Cleaning](/images/median2.png)

## After Cleaning
![Data Cleaning](/images/image4.png)

# RESULT
Thus the given data is read, cleansed and the cleaned data is saved into the file.


