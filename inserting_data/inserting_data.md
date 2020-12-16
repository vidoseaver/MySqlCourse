## Inserting Data


### The single insert:

`INSERT INTO table_name(column_name) VALUE (data);`

Example:

`INSERT INTO cats(name, age) VALUES ('Jetson', 7);`


### The multi insert

```
INSERT INTO table_name 
            (column_name, column_name) 
VALUES      (value, value), 
            (value, value), 
            (value, value);
```

### Note about inserting varchars with quotes:


#### You can do it a couple of ways:

Escape the quotes with a backslash: 

`"This text has \"quotes\" in it"` 

or

 `'This text has \'quotes\' in it'`

Alternate single and double quotes:

`"This text has 'quotes' in it"`

 or

`'This text has "quotes" in it'`

### NULL and NOT NULL 
By default when creating a table rows will be able to have NULL values.

This is show in Null column when using `DESC table;`

If you have a column where null is YES, then when a row is inserted and the value is not defined it will be null.

If you have a column where null is NO, then when you try to generate a row with a default, for varchars that would be an empty string and for int it would be 0

When creating a table you can you make the decision on whether columns can me null or not by setting NOT NULL like so

```
CREATE TABLE cats
    (
        name VARCHAR(20) NOT NULL,
        age INT NOT NULL
    )
```

### Defaults

Like NULL and NOT NULL defaults allow you to provide a default attribute for the tables column on creation. This way instead of getting a empty string, a 0 or NULL you can automatically set the value if it has not been entered.


``` 
CREATE TABLE cats 
    (
        name VARCHAR(20) DEFAULT 'tbd',
        age INT DEFAULT 99
    )
```

### NOTE On NOT NULL AND DEFAULT

You can do NOT NULL and DEFAULT when CREATING a table. IF you do simply does not allow you to insert a NULL value, this can be used as a way to require values.

### Primary Keys

If you want your table to primary keys you need to create it with something like this.
```
CREATE TABLE unique_cats
    (
        id INT NOT NULL,
        name varchar(50),
        age INT,
        PRIMARY KEY (id)
    )
```

#### Auto Incrementing id's
If you don't want to have to pass a primary key every time and keep track of it. Use auto increment

```
CREATE TABLE unique_cats
    (
        id INT NOT NULL AUTO_INCREMENT,
        name varchar(50),
        age INT,
        PRIMARY KEY (id)
    )
```