## SQL Server Section 7
UNION and UNION ALL

```sql
--get Employees wheather the Employee is duplicated it will duplicate
SELECT * FROM EmployeesInSales
UNION ALL
SELECT * FROM EmployeesInAccounting
```
```sql
-- get Employees but is not duplicated
SELECT * FROM EmployeesInSales
UNION 
SELECT * FROM EmployeesInAccounting

```
*Union and Union All is the same in execution plan but Union All convert it to distinct so Union is better performance .*