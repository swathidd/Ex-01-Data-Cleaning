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

# CODE:
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```

# OUPUT
## DATA
![d1](https://user-images.githubusercontent.com/120440439/226254261-8603aa45-22ac-43b9-8089-0bf0fe3fc8d0.png)

## NON NULL BEFORE

df.info

![non](https://user-images.githubusercontent.com/120440439/226255200-ccb21bf0-bba4-467c-9c59-bae6b039e6d6.png)

## MODE
![Screenshot 2023-03-20 110913](https://user-images.githubusercontent.com/120440439/226256267-c48ff7a0-4576-4d78-9597-799daf39eefa.png)

## MEAN
![image](https://user-images.githubusercontent.com/120440439/226257459-369288ca-0850-40ad-a326-323281454bef.png)

## MEDIAN
![Screenshot 2023-03-20 111923](https://user-images.githubusercontent.com/120440439/226257658-00362153-f626-4fb0-98a6-34aafedaabd1.png)

# NON NULL AFTER

df.info()

![image](https://user-images.githubusercontent.com/120440439/226258118-690130f3-9cd2-4fc9-90a6-f5eb47f744f7.png)

df.isnull().sum()

![image](https://user-images.githubusercontent.com/120440439/226258313-4343e680-09ad-447f-a57d-b54c4f21148c.png)

# RESULT:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.






