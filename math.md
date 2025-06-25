---
title: 5. Calculations and Aggregate Functions
nav_order: 6
---

##  Doing Math in SQL: Calculations and Aggregate Functions
SQL isn't just for storing and retrieving data — you can also **do math** with it! Whether you’re adding numbers, calculating averages, or counting records, SQL provides a variety of tools to help.
#### Basic Math Operations

You can do simple math directly in a `SELECT` statement:

```sql
SELECT 4 + 2;
-- Output: 6
```
You can use:
-  __+__ for addition
-  __-__ for  subtraction
-  __*__ for multiplication
-   / for division
-  % for modulo

Unless you include decimal points (e.g., 4.0 / 2), SQL will assume you're working with integers.

---
#### Comparison Operators
These help you compare values:

| Operator | Meaning |
|----------|---------|
| =| Equal to |
| != | Not equal to |
| <> | Not equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal |
| <= | Less than or equal |

---
#### Aggregate Functions

| Function | What it does | Example |
|----------|--------------|---------|
| **SUM()** | Adds up all values in a column | SELECT SUM(price) FROM products; |
| **AVG()** | Calculates the average | SELECT AVG(age) FROM users; |
| **COUNT()** | Counts how many rows (or values) exist | SELECT COUNT(*) FROM students; |
| **MAX()** | Finds the largest value | SELECT MAX(score) FROM results; |
| **MIN()** | Finds the smallest value | SELECT MIN(score) FROM results; |

*Note!* You cannot use aggregate functions in the **WHERE** clause.
