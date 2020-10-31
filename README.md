   # Table of Contents
   * [General-Info](general-info)
   * [Setup](setup)
   * [Environment](environment)
   * [Main functions](main)
       * [CASE](case)
      * [CASTING](casting)
      * [DISTINCT](distinct)
   * [Screenshots](screenshots)
   * [Queries](queries)
<br>

## General - Info 

    This project was created in order to understand the basic,
    cleaning process in SQL, with some important functions in result of exploring the dataset,
    get duplicate values etc.
    <br>
    
## Setup
    In order to start the project do the following:
       1. Start Microsoft SQL Server Management Studio
       2. Click Databases
       3. New Database 
       4. Give your new database a name 
       5. Start designing
## Environment
```
SQL Server Management Studio 2018
SQL Server 2019
```
## Main functions for cleaning
CASE

  **Function Defining**
    
    WHEN specific variables satisfy specific criteria THEN,  
    they take the label name that the user provides.
    
   **FORMAT**
   ```SQL
CASE
    WHEN condition1 THEN value1
    WHEN condition2 THEN value2
    ...
    WHEN conditionX THEN valueX
    ELSE else_value
END
```

## CASTING

**Function defining**
    
    Changing the data type of a column within  a query.Let's say,
    we want to change the data type of a variable age to numeric format.
    
**FORMAT**
    
    SELECT
        X1,
        X2,
        age::TEXT
    FROM
    Table
       
DISTINCT
=
**Function defining**
    
    Determining the unique values in a dataset.
    
**FORMAT**    
    
    SELECT
        DISTINCT X1
    FROM
        Table

## Screenshots
![database](https://user-images.githubusercontent.com/47696240/96724398-756e3880-13b8-11eb-8081-cf9119f1f56e.png)
<br>

![reviews under 310](https://user-images.githubusercontent.com/47696240/96724984-13fa9980-13b9-11eb-9071-88c8e48d1d89.png)



## Queries

### Finding the distinct courseProviders  from db 
```SQL
SELECT DISTINCT(CourseProvider) AS distinct_values
FROM newCleaning
```
### Function CASE
```SQL
SELECT TotalReviews,
CASE 
WHEN TotalReviews <= 16 THEN 'Not reliable course'
WHEN TotalReviews <= 455 THEN 'Some reliable course'
ELSE 'Very reliable course'
END AS CaseStatement
FROM newCleaning
```
