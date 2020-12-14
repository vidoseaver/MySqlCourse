Creating Databases: Code

Create a table:

```
CREATE TABLE tablename
    (
        column_name data_type,
        column_name data_type
    )
```

NOTE:
tablename should be pluralized, don't forget the comma's after the data_type

Example:
```
CREATE DATABASE cats 
    (
        name varchar(100),
        age int
    )

