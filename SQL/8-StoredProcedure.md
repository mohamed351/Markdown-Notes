## SQL Server Section 8
### Stored Pricedure
*a stored procedure is group of t-sqll transaction sql statement. if you have a situation you write the same query over and over again you can save specific query as a procedure and call it just by it's name*
### Example about stored procedure
```sql
CREATE PROC SP_GET_Employees
as
BEGIN 
    SELECT * FROM Employees
END
-- or 
CREATE PROCEDURE SP_GET_Employees
as
BEGIN 
    SELECT * FROM Employees
END
-- To execute store procedure 
EXEC SP_GET_Employees
--OR
EXECUTE SP_GET_Employees
```
## To make Stored Procedure with Paramter
```sql
CREATE PROC SP_GET_Employees_With_ID
@EmployeeID as int
as
BEGIN 
    SELECT * FROM Employees WHERE ID= @EmployeeID
End 
```
### To make Specify  Paramter 
```sql
CREATE PROC SP_GET_Employee
@DepartmentID as int,
@Gender as nvarchar(20)
as
BEGIN
    SELECT * FROM Employees WHERE 
    DepartmetID =@DepartmentID AND 
    Gender =@Gender
END

EXECUTE SP_GET_Employee @DepartmentID =1,
@Gender ='Male';
```
```sql
EXEC sp_helptext SP_GET_Employee
EXEC sp_helptext SP_GET_Employee  1,'male' -- if you want to add 

```
### Alter Procedure 
```sql
ALTER PROC spGenderEmployees
AS
BEGIN 
    Select * FROM Employees
    WHERE Gender ='male'
END
```
### Drop Procedure 
```sql
DROP PROC spGenderEmployees

```
### To Create Procedure With Encryption
```sql
ALTER PROC spGenderEmployees
@Gender nvarchar(20)
WITH ENCRYPTION
as
SELECT * FROM Employees Where Gender ='male';

```

