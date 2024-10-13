# AdventureWorks_PythonProject
This respository contains a Jupyter Notebook that demonstrates how to perform data cleaning and exploratory data analysis (EDA) on a dataset imported from SQlite database.

## Importing Data from SQlite
In Jupyter Notebook, I connect to SQlite database, load data into pandas DataFrames, and perform various data cleaning and analysis tasks.

## Steps to Import Data from Sqlite
Import the necessary libraries, such as pandas for data manipulation, numpy for numerical computations and sqlite3 for connecting to the SQlite database. Established conection to SQlite databass using the sqlite3.connect () functiom, specifying the path to the database file. The connection was exceuted, run SQL queries to extract the tables from the database. After loading the tables, the connection was closed. Finally the first few rows of each DataFrame using the .head() to ensure the data was loaded correctly.

## Checked Columns and Data Types
After the table was loaded, checked datatypes and columns using .info() to give the summary of the table which includes count, null value and datatype, and also corrected the datatypes that are not appropriate,

## Handled Missing Values
Handled missing values in the tables ensuring no nulls by checking the sum of missing values in each column using .isnull().sum() function. For numerical columns with missing values, were filled with column mean to maintain consistency in dataset.

## Referential Integrity
Ensured that foreign key values in one table match primary key values in corresponding tables preventing invalid realtionships.

## Outliers
Identified outliers in the product table by creating boxplot using seaborn. The boxplot helps to visualize the spread of the data and highlights the values that lie far outside the InterQuartile Range(IQR).Calculated the IQR for the product price and define the upper and lower bound based on the IQR rule(1.5 times the IQR) to handle the outliers. Values outside lower and upper bound are the outliers and are removed from the dataframe to ensure a cleaned analysis.

## Explanatory Data Analysis
Peformed explanatory data analysis to check for the column in dataframes using .describe() function to provide the summary of the tables. Finally, after completing the data cleaning, referential integrity and explanatory data analysis, saved the cleaned data back to CSV file for future reference.

## Conclusion
This project demonstrates the key aspects of data cleaning, includfing missing values, ensuring referential integrity, managing outliers and perform exploratory data analysis. These steps ensure the dataset is of high quality and ready for deeper analysis.

**THANK YOU**!!


