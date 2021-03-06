## Microsoft SQL Server - Section 3
### Insert Data On Table

```sql
INSERT INTO [TABLE_NAME] ([COLUMN_NAME], [COLUMN_NAME]) VALUES ([COLUMN_VALUE]. [COLUMN_VALUE]);
```
#### Example about Employees Table 
*Employees Table has 3 columns ID, Name and Salary ID is Auto Increment*
```sql
INSERT INTO Employees (Name,Salary) VALUES ('Mohamed',3000);
```
## Default Constraint
### Example about Employee
*create a default salary if employees is Inserted without salary make salary equal 1000*
```sql
 ALTER TABLE Employees 
 ADD CONSTRAINT DF_Employees_Salary DEFAULT 1000 FOR
Salary
```
## Drop Constraint 
```sql
ALTER TABLE Employees
DROP CONSTRAINT DF_Employees_Salary
````

## Cascading Referential Integrity
*the Default of Cascading is [NO ACTION] which is throw exception when you delete*
#### Types of Referential Integrity
- NO ACTION
- CASCADE
- SET NULL 
- SET DEFAULT
```sql
ADD CONSTRAINT fk_SalesHistoryCustomerID FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID) ON DELETE SET NULL ON UPDATE SET NULL

ALTER TABLE SalesHistory

ADD CONSTRAINT fk_SalesHistoryProductID FOREIGN KEY (ProductID) REFERENCES Products(ProductID) ON DELETE CASCADE ON UPDATE CASCASE
````
### Check Constraint
*if you want to create check constraint* 
```sql
ALTER TABLE [TABLE_NAME]
ADD CONSTRAINT [CONTSTRAINT_NAME] CHECK [BOOLEAN_EXPRESSION]
```
*if you want to drop check constraint*
```sql
ALTER TABLE [TABLE_NAME]
DROP CONSTRAINT [CONTSTRANT_NAME]
```
### Unique Key Constraint
*Add constraint unique in table*
```sql
ALTER TALBE [TABLE_NAME]
ADD CONSTRAINT [CONSTRAINT_NAME] UNIQUE([COLUMN_NAME])
``` 
### drop constraint
```sql
ALTER TABLE [TABLE_NAME]
DROP CONSTRAINT [CONSTRAINT_NAME]

```



