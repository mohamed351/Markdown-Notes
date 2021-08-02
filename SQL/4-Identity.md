## Microsoft SQL Server - Section 4
## Identity Column 
 *Identity Increment : how many to increment 
Identity seed : the starting point*
*if you want to make Identity Insert it atuomaticlly on*
```sql
set Identity_insert Employees off

```
*if you want to make Identity Insert it atuomaticlly off*
```sql
set Identity_insert Employees on
```
*there is another code for disable Identity column to fill the gaps*
```sql
DBCC CHECKIDENT([TABLE_NAME],RESEED,0)
```
*to get the last identity Value column*
```sql
SELECT @@IDENTITY 
SELECT SCOPE_IDENTITY()
SELECT IDENT_CURRENT('TABLE_NAME')
```
*  @@IDENTITY : Same Session and across any scope
- SCOPE_IDENTITY() : Same Session and the same scope 
- IDENT_CURRENT('Table') :a specific table a cross any session and any scope.




