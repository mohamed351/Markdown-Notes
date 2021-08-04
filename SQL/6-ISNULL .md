## Microsoft SQL Server - Section 6
## Handele Null
```sql
SELECT ISNULL( religion,'NOT Specified') FROM Employees
SELECT COALESCE(Email, 'NOT Specified') FROM Employees
```
----------------------------------
## Case When
```sql
SELECT 
CASE WHEN <Expression> THEN '' ELSE '' END
 FROM Employees

```
*you can use case and else for NULL VALUES*
## Example
```sql
SELECT 
CASE WHEN [Name] is NULL THEN '' ELSE '' END
 FROM Employees
```
------------------------------------
## COALESCE Function
```sql
SELECT COALESCE(FirstName, LastName,MiddleName,'Not Specified') FROM Employees
```
*if first name is null is going to take last name and if middle Name is null is going to take Not Specifited*
