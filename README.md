# Ex-01_DS_Data_Cleansing:


## AIM:
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant,duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM:

### STEP 1:
Read the given Data
### STEP 2:
Get the information about the data
### STEP 3:
Remove the null values from the data
### STEP 4:
Save the Clean data to the file


# CODE:
~~~
Developed by:R.SOMEASVAR.
Register number:212221230103.

import pandas as pd
df=pd.read_csv("Data_set.csv")
df.head(10)
df.tail()
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['show_name'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.head()
df.info()
~~~
# OUPUT:
DATA :

![output](./data.jpg)

NON-NULL COUNT BEFORE :

![output](./beforenull.jpg)

NULL SUM :

![output](./null.jpg)

UPDATED DATA :

![output](./air.jpg)

NON-NULL COUNT AFTER :

![output](./after.jpg)

## RESULT:
The given data has been read and data cleaning has been performed and saved the cleaned data to a file.





