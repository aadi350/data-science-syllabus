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

