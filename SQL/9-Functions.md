## Microsoft Sql Server  -Section 9
## Functions
*if you want to create function in sql microsoft sql that returns table*
```sql
CREATE TABLE GET_Employee(@EmployeeID as INT)
returns Table
return (
SELECT * FROM Employees where ID =@EmployeeID
)
```