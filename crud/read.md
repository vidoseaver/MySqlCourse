## Reading data out

### Various Simple SELECT statements:

`SELECT * FROM tablename;`

Gives all records with all columns from that table name.

`SELECT column_name_1 FROM tablename;`

Give only column 1 info for all records from that table

`SELECT column_name_1,column_name_2 FROM tablename`

Gives both column 1 and column 2 info from that table for all records

### Where

Where allows you to select by a certain value. So something like 

` SELECT * FROM tablename WHERE columnname=value;`

#### NOTE:

The value statement above needs to be in quotes if its a string

Its case insensitive

Can use other columns like variables
    example
    `SELECT * FROM cats WHERE cat_id=age;`

### Aliases

You can rename columns when selecting

`SELECT id AS cat_id FROM cats`



