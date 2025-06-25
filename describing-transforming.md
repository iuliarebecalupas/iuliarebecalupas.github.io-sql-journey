---
title: Describing and Transforming the Data
nav_order: 7
---

## Describing and Transforming Data in SQL

###  Describing the Data

| Function | What it does | Example |
|----------|--------------|---------|
|**LENGTH()** | Returns the number of characters in a string. | ``` SELECT LENGTH('Hello') AS name_length;  ``` |
| **DISTINCT** | Removes duplicates from the result set, showing only unique values. | ``` SELECT DISTINCT city FROM customers; ``` |
| **COUNT()** | Counts the number of records, or non-null values in a column. | ``` SELECT COUNT (*) FROM students; ``` |

---
### Transforming the Data

| Function | What it does | Example |
|----------|--------------|---------|
| **LOWER()** | Converts text to lowercase. | ``` SELECT LOWER('SQL IS FUN') AS lowercase_text; ``` |
| **UPPER()** | Converts text to uppercase. | ``` SELECT UPPER('sql is fun') AS uppercase_text; ``` |
| **SUBSTR()** or **SUBSTRING()** | Extracts part of a string. | Get first 3 characters of a name: ``` SELECT SUBSTR('Jonathan', 1, 3) AS short_name; ``` -> Output: Jon | 
| **REPLACE()** | Replaces part of a string with something else. | ``` SELECT REPLACE ('Jules', 'e', 'y') FROM students; ``` -> Output: Julys
| **CAST()** | Tells the data base to interpret one data type as another | ``` SELECT age FROM students ORDER BY CAST (age AS CHAR); ``` |
---
### Creating Aliases with **AS**

You can change the return name of a field (column) with the **AS** keyword.

``` SELECT last_name AS lastname FROM students; ```



