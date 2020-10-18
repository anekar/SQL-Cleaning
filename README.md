   # Table of Contents
   * [General-Info](general-info)
   * [Setup](setup)
   * [Environment](environment)
   * [Main functions](main)
       * [CASE](case)
      * [COALESCE](coalesce)
      * [NULLIF](nullif)
      * [LEAST](least)
      * [GREATEST](greatest)
      * [CASTING](casting)
      * [DISTINCT](distinct)
    
   * [Screenshots](screenshots)
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
= 
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
## COALESCE

  **Function Defining**
    
    Replacing null values with standrard values.
  
 
**FORMAT**
```SQL
SELECT
    X1,
    X2,
    COALESCE(title, 'NO TITLE') AS title
FROM
    table
```

## NULLIF

   **Function defining**
    
    This function is the opposite of COALESCE.
    If the first value equals the second it will return NULL. 
  **FORMAT**
  
    SELECT
       X1,
       X2,
       NULLIF(Condition1, 'Variable') AS ...
    FROM
        Table

## LEAST

  **Function Defining**
    
    This function takes any number of values and returns the least,
    of the values. For example say the greatest amount is 15.
    
   **FORMAT**
    
    SELECT
       X1,
       X2,
       X3,
       X4,
       X5
       LEAST(15, wage) as ...,
       ...
    FROM
       employees;
  
   
## GREATEST     
   
**Function Defining**
    
    This function takes any number of values and returns the greatest,
    of the values. For example say the least amount is 15.
    
   **FORMAT**
    
    SELECT
       X1,
       X2,
       X3,
       X4,
       X5
       GREATEST(15, wage) as ...,
       ...
    FROM
       employees;
       
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
