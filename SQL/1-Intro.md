## Microsoft SQL Server 

- *There is two types of authication in sql server one is windows autication and the mixed mode*
- *There is a difference between sql server managment studio and sql server engine database*
- *if you want to install sql Server please Search in Google*

### Create Altering and Dropping a Database 
> [Note]
> Every Query or Creating a Database Can be done by Sql server Management Studio But you need to learn In Code and It is better we are not going to Discuss GUI
 
#### Creating a Database 
```sql
CREATE DATABASE [NAME_OF_DATABASE]
``` 

> [Note]
> There is a System Database Please Don't Delete them 
> Which is master , model , msdb, tempdb
> We are going to Discuss What is the benefit of them 
> it is provided by sql server

*In Every Database We Created there is 2 files for Database one is mdf file which has a data and ldf which has a Transaction Log File*

#### Change the Name of Database

```sql
ALTER DATABASE [NAME_OF_DATABASE]
MODIFY NAME = [NEW_NAME_OF_DATABASE]
```
*another way of modifiy database is using stored prodcure*
```sql
EXECUTE sp_renameDB 'OLD_NAME', 'NEW_NAME'
```

*for dropping database " deteting database  you have"*


```sql
DROP DATABASE [DATABASE_NAME]
```
*Remember when you dropping a database the database shouldn't be used
you will get an Error 

'you cannot drop a database because it is currently use'*

*To Delete a Database you need to change to SINGLE_USER*

#### Change the Database To Single User
```sql
ALTER DATABASE [DATABASE_NAME] 
SET SINGLE_USER WITH ROLLBACK IMMEDIATE
```
*Then Drop The Database is going to be dropped*







