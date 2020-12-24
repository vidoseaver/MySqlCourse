# String Functions

String functions, only change the query output, they don't affect the actual data in the database.



## Concat

Use concat to combine strings

```
SELECT
    CONCAT(column_1, maybe-a-space, column_2) as whatever-you-want-to-call-it
FROM tablename;
```

## CONCAT_WS

Concat with separator

```
SELECT
    CONCAT_WS(separator(i.e ','), column_1, column_2) as whatever-you-want-to-call-it
FROM tablename;
```

## SUBSTRING or SUBSTR()

Use with column names

```
SELECT SUBSTRING(column-name, 1, 10) FROM tablename;
```
NOTE: you can use `as your-new-columname` with it

### With starting and ending index.

This will return the a string of the letters including both indices

```
SELECT SUBSTRING('Some word', starting-index, ending-index)
```
Note the starting index is 1 instead of 0



### With Single index

This will return everything after that index

```
SELECT SUBSTRING('Some word', index-to-start-from)
```

### With single negative index

this will return that index count back from the end of the string.

```
SELECT SUBSTRING('Some word', -positions-to-count-back)
```

## Replace

Replace replaces a substring in a string with another substring

``` 
SELECT REPLACE(full-string, substring-replace, replacing-substring)
```

## Reverse

Reverses a string

```
Select REVERSE(string)
```

## CHAR_LENGTH

Returns the an int of the number of characters in a string.

```
SELECT CHAR_LENGTH(string)
```

## UPPER & LOWER
Changes string case to upper or lower case.
```
SELECT UPPER(String)