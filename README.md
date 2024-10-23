# AdventureWorks_PythonProject
This respository contains a Jupyter Notebook that demonstrates how to perform data cleaning and exploratory data analysis (EDA) on a dataset imported from SQlite database.

## Importing Data from SQlite
In Jupyter Notebook, I connect to SQlite database, load data into pandas DataFrames, and perform various data cleaning and analysis tasks.

## Steps to Import Data from Sqlite
Import the necessary libraries, such as pandas for data manipulation, numpy for numerical computations and sqlite3 for connecting to the SQlite database. Established conection to SQlite databass using the sqlite3.connect () functiom, specifying the path to the database file. The connection was exceuted, run SQL queries to extract the tables from the database. After loading the tables, the connection was closed. Finally the first few rows of each DataFrame using the .head() to ensure the data was loaded correctly.

## Tools
Pandas: For data manipulation and cleaning.

Matplotlib/Seaborn: Used for data visualization.

SciPy/Statsmodels: For statistical analysis and hypothesis testing.

Jupyter Notebook: Environment for running and documenting the analysis.

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

## Sales and Customer Analysis
Performed time series analysis on Sales data, extracted the year and month from sales data table OrderDate. Joined the sales table and the products table together to calculate the TotalSales. Finally visualize and plot total sales by year and month.

## Top Performing Products and Regions 
Examined the sales distribution across the region and year, filtered the date by date and then group by product and region. Also analyze product performance across different region and years grouping the data by both region and year. Then visualize the top product and year and also region and year.

## Customer Demographics and Purchasing Pattern
Merged the sales table with the customer demographic data and analyze to understand their purrchasing patterns, customer behaviour, and their preferences.

## Customer Segmentation
Performed based on purchasing power and spending bahaviour. Divide customers into segments based on their total spending, allows us to identify high-value customers and their contibution to overall sales.

## Product Performance and Trends
Analyzed the performance of various products by grouping the sales data based on product name. The analysis identidy the product performance over time by total sales and the number of orders.

## Sales Performance and Trends
Analyze sales performance across the regions to identify high performing and low performing region. Aggregated the total sales by regions and visualize the results to understand the trends and differences in performance across the various territories.

## Hypohesis Testing
Performed ANOVA(Analysis of Variance) to determine the difference in sales performance across different regions. We used the **F-statistic** and the **P-value** to access the variance between the regions. The hypothesis testing help us determine the variations in sales across the region are statistically significant or they occur due to random chance. We concluded that sales performance does vary across between the region.

## Advanced Statistical Analysis 
**Linear Regression**
Performed linear regression to understand the relationship between product price and sales.

** Correlation Analysis**
Performed correlation analysis to analyze the correlation between Product Price and sales.

##

## Conclusion
This project demonstrates the importance of clean and well-structured data for effective data analysis. By following rigorous data cleaning procedures as handling missing values, ensuring referential integrity and managing outliers, including time series analysis, customer segmentation and product performance trends. By utilizing python libraries we were able to gain crucial insights into sales performance, customer bahaviour and regional trends. Additionally, we applied advanced statistical techniques allowing for a deeper understanding of the relationships between different various variables.

**THANK YOU**!!


