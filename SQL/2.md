## Microsoft SQL Server - Section 2
### CREATE TABLE
```sql
CREATE TABLE [TABLE_NAME](
[COLUM_NAME] [DATA_TYPE] [ALLOW_NULL_OR_NOT] [PRIMARY KEY], 
[COLUMN_NAME] [DATA_TYPE] [ALLOW_NULL_OR_NOT] 
 
)
```
#### Example Create table Gender
```sql
CREATE TABLE Gender(
ID INT NOT NULL PRIMARY KEY,
[NAME] NVARCHAR(50) NOT NULL
)
```
### Creating Table With Relationship 
![](https://github.com/mohamed351/Markdown-Notes/blob/master/SQL/relation.png)

```sql
CREATE TABLE employees(
employee_id INT PRIMARY KEY IDENTITY(1,1),
first_name NVARCHAR(50),
last_name NVARCHAR(50),
email NVARCHAR(50),
phone_number NVARCHAR(50),
job_id INT,
salary INT,
manager_id INT,
department_id INT
)

CREATE TABLE departments(
department_id INT PRIMARY KEY,
department_name NVARCHAR(50),
location_id INT
)
--to create relationship between employees add department 
ALTER TABLE employees
ADD CONSTRAINT employees_department_id FOREIGN KEY (department_id) REFERENCES departments(department_id)

```


