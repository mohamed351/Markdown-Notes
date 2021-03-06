## Microsoft SQL Server - Section 5
### Select Statement
```sql
SELECT * FROM People

```
### select distinct
*show the all city without duplicated*
```sql
SELECT DISTINCT City FROM People
```
### select where 
```sql
SELECT * FROM People WHERE City= 'London'
GO
SELECT * FROM People WHERE City <> 'London'
GO
SELECT * FROM People WHERE City != 'London'
```
*there is another operators used in where*
|Operator|Purpose|
|--------|-------|
| = |Equal|
| != or <> | Not Equal|
| > | Greater Than|
| < | Less Than|
| <=|Less than or Equal|
|IN | Specify a list of values|
|BETWEEN| Specify a range|
|LIKE| Specify a pattern|
|NOT| Not in list , range etc..|
----------------------------
|Operator|Purpose|
|--------|-------|
| %|Specify zero or more characters|
|-|Specify exactly one character|
|[]|any character with in the brackets|
|[^]|Not any character with in the brackets|
---------------------------
|Operator|Purpose|
|--------|-------|
|AND | -|
|OR | -|
---------------------------
### Example for Simplifying The Query 
```sql
SELECT * FROM People WHERE Age =20 OR Age = 30 OR Age =25;
-- you can make it simple
SELECT * FROM People WHERE Age IN(20,30,25); 
-- you can use between 
-- getting all People that age between 20 , 30
SELECT * FROM People WHERE Age BETWEEN  20 AND 30
```
### Example for Like Operator
```sql
-- start with letter L
SELECT * FROM People WHERE City LIKE 'L%' 
-- any character in Word
SELECT * FROM People WHERE Email LIKE '%@%'
-- you can use NOT Operator
SELECT * FROM People WHERE Email NOT LIKE '%@%'
-- One Character after the @ symbole 
SELECT * FROM People WHERE Email LIKE '_@'
-- A@A.com
SELECT * FROM People WHERE Email LIKE '_@_.com'
-- get Name start with M , S ,T like 
 SELECT * FROM People WHERE [Name] LIKE '[MST]%'
-- Does not equal get Name start with M , S ,T like 
 SELECT * FROM People WHERE [Name] LIKE '[^MST]%'
```
### Example about ORDER BY
```sql
SELECT * FROM People WHERE [Name] LIKE '[MST]%' 
ORDER BY [Name]
-----------------------------------------------
SELECT * FROM People WHERE [Name] LIKE '[MST]%' 
ORDER BY  [Name] DESC , [Age] ASC , 
```
### Keyword Top
```sql
SELECT TOP 10 * FROM People 
SELECT TOP 10 PERCENT *  FROM  PEOPLE
```

### Aggregate Functions

|Function|Operator|
|--------|--------|
|APPROX_COUNT_DISTINCT| - |
|AVG | Get Avrage|
|CHECKSUM_AGG|-|
|COUNT|Get Count|
|COUNT_BIG|-|
|GROUPING|-|
|GROUPING_ID|-|
|MAX|Get Max|
|MIN|Get Min|
|STDEV|-|
|STDEVP|-|
|STRING_AGG|-|
|SUM|Get Sum|
|VAR|-|
|VARP|-|
----------------------------
#### Example 
```sql
-- calculate the salaries across the table 
SELECT SUM(Salary) FROM Employees
-- Get the count of Employees
SELECT COUNT(*) FROM Employees
--but for performace use this query 
SELECT COUNT(ID) FROM Employees
```
 
### Group By 
*Group by clause is used to group a selected set of rows into set of summary rows by the values one or more columns or expressions .it is alwats used in conjunction with one or more aggregate functions*

```sql
--write a query what  total salary across the city
SELECT City , SUM(Salary) FROM Employees
```
### Having 
1. where clause can be used with-Select ,Insert , and Update statement where as Having caluse can only be used with Select statment 
2. Where filter rows before aggregation (GROUPING) where as , Having filter group   
### Joins
1.INNER JOIN
2.OUTER JOIN
3.CROSS JOIN
--------------------------------
![](https://github.com/mohamed351/Markdown-Notes/blob/master/SQL/Photos/1.png)
 




