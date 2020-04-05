Basic usage:

```mysql
CREATE DATABSE database_name;
USE database_name;
DROP DATABASE database_name;
SHOW DATABASES;
SHOW TABLES;
DESCRIBE table_name; # show table’s organization 
```

summarize number of different values:
```mysql
SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
```
