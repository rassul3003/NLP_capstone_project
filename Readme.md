# **Introduction**

This data science project aims to classify the strength of passwords using machine learning algorithms. 
Password strength is determined based on various features, including the length of the password and the frequency of lowercase characters, uppercase characters, numeric characters, and special characters.


## __Project Steps__

### _1. Data Retrieval_

The project begins by connecting to an SQLite database to retrieve password data.

```
import pandas as pd
import sqlite3

# Create an SQL connection with SQLite database
connection = sqlite3.connect(r'C:\Users\rassu\NLP_capstone_project\password_data.sqlite')

# Store the database data into 'data' dataframe
data = pd.read_sql_query("SELECT * FROM Users", connection)

```
### _2. Data Cleaning_

2.1Irrelevant features are removed from the dataset.

```
data.drop(['index'], axis=1, inplace=True)
```
2.2 Check for Duplicate Rows
Check for and handle duplicate rows if present.

2.3 Check for Missing Values
Verify if there are any missing values in the dataset and handle them as needed.

2.4 Check Data Type of Every Feature
Ensure that the data types of all features are appropriate for analysis.

2.5 Check If 'strength' Column Has Irrelevant Values
Examine the 'strength' column for any irrelevant values.

### _3. Semantic Analysis_

Perform semantic analysis to understand the nature of passwords in the dataset.
```
a) How many passwords consist of only numeric characters?
b) How many passwords consist of only uppercase characters?
c) How many passwords consist of only alphabetic characters?
d) How many passwords consist of alpha-numeric characters?
e) How many passwords consist of title-case characters?
f) How many passwords consist of some special characters?
```

### _4. Feature Engineering_

Define the features that contribute to password strength:
```
Length of password
Frequency of lowercase characters
Frequency of uppercase characters
Frequency of numeric characters
Frequency of special characters
```

### _5. Perform Descriptive Statistics_

Determine the statistics of features in predicting password strength.

### _6. Feature Importance_

Determine the importance of features in predicting password strength.

### _7. Apply TF-IDF on Data_

Apply Term Frequency-Inverse Document Frequency (TF-IDF) transformation if relevant for your project.

### _8. Apply Machine Learning_

Build and train machine learning models to classify password strength.

### _9. Prediction on Sample Data_

Apply the trained model to make predictions on sample data.

### _10. Model Evaluation_

Evaluate the model's performance using appropriate metrics and techniques.

