# DELETE vs TRUNCATE
Delete removes a table row, and can be rolledback, Truncate deletes all rows and cannot be rolled back  

# Constraints  
This is an optional part of a ```SQL CREATE`` or ```SQL ALTER``` statement, it enforces a rule to which data must conform  
## Column Constraints  
**NOT NULL**   
Specifies that this column cannot hold NULL values (constraints of this type are not nameable).  
**PRIMARY KEY**  
Specifies the column that uniquely identifies a row in the table. The identified columns must be defined as NOT NULL.  
**UNIQUE**  
Specifies that values in the column must be unique.  
**FOREIGN KEY**  
Specifies that the values in the column must correspond to values in a referenced primary key or unique key column or that they are NULL.  
**CHECK**  
Specifies rules for values in the column.
## Table Constraints  
**PRIMARY KEY**  
Specifies the column or columns that uniquely identify a row in the table. NULL values are not allowed.  

**UNIQUE**  
Specifies that values in the columns must be unique.

**FOREIGN KEY**  
Specifies that the values in the columns must correspond to values in referenced primary key or unique columns or that they are NULL.  

Note: If the foreign key consists of multiple columns, and any column is NULL, the whole key is considered NULL. The insert is permitted no matter what is on the non-null columns.  

**CHECK**  
Specifies a wide range of rules for values in the table.  
# Joins
**INNER**  
Combines common between two or more tables  
```SQL
SELECT columns
FROM table1 
INNER JOIN table2
ON table1.column = table2.column;
```
**LEFT OUTER**  
Returns all rows from left table, and only rows from the other table which match left table rows  
```SQL
SELECT columns
FROM table1
LEFT [OUTER] JOIN table2
ON table1.column = table2.column;
```  
**FULL OUTER JOIN**  
Returns all rows from left and right tables with nulls in place for non-matching rows  
```SQL
SELECT columns
FROM table1
FULL [OUTER] JOIN table2
ON table1.column = table2.column
```
# Group By
Groups a result into subsets matching values for one or more columns, in each group, no two rows have the same value for grouping columns  

## Rollup Syntax  
Allows multiple group-by's  
```SQL  
GROUP BY 
{
columnName [ , columnName ]*  
|
ROLLUP ( columnName [ , columnName ]* )
}
```

## Aggregate Functions
```SQL
-- find the average flying_times of flights grouped by
-- airport
SELECT AVG (flying_time), orig_airport
FROM Flights
GROUP BY orig_airport

SELECT MAX(city_name), region
FROM Cities, Countries
WHERE Cities.country_ISO_code = Countries.country_ISO_code
GROUP BY region

-- group by an a smallint
SELECT ID, AVG(SALARY)
FROM SAMP.STAFF
GROUP BY ID

-- Get the AVGSALARY and EMPCOUNT columns, and the DEPTNO column using the AS clause
-- And group by the WORKDEPT column using the correlation name OTHERS
SELECT OTHERS.WORKDEPT AS DEPTNO,
AVG(OTHERS.SALARY) AS AVGSALARY,
COUNT(*) AS EMPCOUNT
FROM SAMP.EMPLOYEE OTHERS
GROUP BY OTHERS.WORKDEPT

-- Compute sub-totals of Sales_History data, grouping it by Region, by
-- (Region, State), and by (Region, State, Product), as well as computing
-- an overall total of the sales for all Regions, States, and Products:
SELECT Region, State, Product, SUM(Sales) Total_Sales
FROM Sales_History 
GROUP BY ROLLUP(Region, State, Product)
```

# Cursors  
Pointer than points to the result of a query  
```SQL
CURSOR cursor_name IS query
```  

**OPEN**  
Cursors must be opened before rows are fetched from the cursor  
```SQL 
OPEN cursor_name  
```  

**FETCH**  
Places the contents of the current row into variables   
```SQL 
FETCH cursor_name INTO variable_list
```  

**CLOSE**  
After fetching rows, cursor must be closed, which releases all allocated memory 
```SQL  
CLOSE cursor_name  
```  

# Filtering using ```WHERE``` or ```HAVING```
# Common Table Expressions
# Case 
# Dates