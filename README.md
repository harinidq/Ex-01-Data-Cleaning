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
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
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

### DATA:

![image](https://user-images.githubusercontent.com/113497680/226850210-6234da79-781c-45a1-a9c3-2311a4d78efb.png)

### NON NULL BEFORE

### df.info:

![image](https://user-images.githubusercontent.com/113497680/226850737-c712e8a8-e5fe-4b44-934b-15cdcaad6a39.png)

### MODE:

![image](https://user-images.githubusercontent.com/113497680/226855689-ec06b6c8-86fa-45da-a54f-bc132474423e.png)

### MEAN:

![image](https://user-images.githubusercontent.com/113497680/226855823-0ff84cdb-1a5b-4b0c-88aa-fa5daf58db4c.png)

### MEDIAN:

![image](https://user-images.githubusercontent.com/113497680/226856074-5b6c4318-9967-4acc-b7c1-86afc128cac9.png)

### NON NULL AFTER:

### df.info:

![image](https://user-images.githubusercontent.com/113497680/226851837-05660315-1603-495b-af81-f797b8a1fadb.png)

### df.isnull().sum():

![image](https://user-images.githubusercontent.com/113497680/226856216-d17bef92-b8f9-4d2e-a87d-de521cecd949.png)

### RESULT:

Thus,the given data is read,cleared and the cleaned data is saved into the file.
