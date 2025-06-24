---
title: SQL Query Essentials
nav order: 3
---

# SQL Query Essentials

This section introduces key SQL commands that are essential for querying and managing data. Each keyword or clause is explained with examples to help you understand how to use them.

---

## SELECT

**What it is:** The `SELECT` statement is used to retrieve data from a database.

**What it does:** Tells the database which columns you want to see.

**Syntax:**

```sql
SELECT column1, column2 FROM table_name;
```

**Wildcard `*`:**

* `SELECT *` means “select all columns.”

**Example:**

```sql
SELECT * FROM customers;
```

> Returns all columns from the "customers" table.

---

## WHERE

**What it is:** A clause used to filter records.

**What it does:** Retrieves only rows that match a specific condition.

**Example:**

```sql
SELECT * FROM customers WHERE country = 'Germany';
```

> Returns all customers from Germany.

---

## AND, OR, IS, and ()

* **AND**: All conditions must be true.
* **OR**: At least one condition must be true.
* **IS**: Used with NULL values.
* **()**: Parentheses group conditions to clarify logic.

**Example:**

```sql
SELECT * FROM customers
WHERE (country = 'Germany' OR country = 'France')
AND age > 30;
```

> Returns customers from Germany or France who are older than 30.

---

## LIKE '%'

**What it is:** Used for pattern matching.

**What it does:** Finds records where a column’s value matches a specified pattern.



**Examples:**

- Starts with a certain pattern
```sql
SELECT * FROM contacts WHERE first_name LIKE 'J%';
```

> Matches any name that starts with "J" (e.g., "James", "Julia", "John").
-   Ends with a certain pattern
```sql
SELECT * FROM contacts WHERE last_name LIKE '%son';
```
> Matches any name that ends with "son" (e.g., "Anderson", "Jackson").
-   Contains a certain pattern anywhere
```sql
SELECT * FROM contacts WHERE first_name LIKE '%ann%';
```
> Matches any name that contains "ann" (e.g., "Joanna", "Gianna").

---

## LIMIT

**What it is:** Restricts the number of results returned.

**What it does:** Limits how many rows you get back.

**Example:**

```sql
SELECT * FROM customers LIMIT 5;
```

> Returns only the first 5 rows.
---
## OFFSET

**What it is and does:** A clause that allows you to skip a number of rows before starting to return rows from a query. It’s often used together with LIMIT.


**Example:**

```sql
SELECT * FROM customers LIMIT 5 OFFSET 5;
```

> Returns 5 customers, skipping the first 5 ones.

---

## ORDER BY

**What it is:** Sorts results by one or more columns.

**What it does:** Organizes your output in ascending (ASC) or descending (DESC) order.

**Default:** ASC (ascending)

**Example:**

```sql
SELECT * FROM customers ORDER BY last_name ASC;
```

> Returns customers sorted by last name from A to Z.

```sql
SELECT * FROM customers ORDER BY age DESC;
```

> Returns customers from oldest to youngest.

---

## JOINs

Joins Asks for records across two tables, based on a related column.

### 1. Implicit JOIN

```sql
SELECT * FROM customers, orders WHERE customers.id = orders.customer_id;
```

> Joins customers with their orders.

### 2. CROSS JOIN

```sql
SELECT * FROM products CROSS JOIN categories;
```

> Returns all possible combinations.

### 3. (INNER) JOIN

```sql
SELECT * FROM customers
INNER JOIN orders ON customers.id = orders.customer_id;
```

> Only returns rows with matches in both tables.

### 4. LEFT (OUTER) JOIN

```sql
SELECT * FROM customers
LEFT JOIN orders ON customers.id = orders.customer_id;
```

> Returns all customers, even those with no orders (nulls in order columns).

### 5. RIGHT (OUTER) JOIN

```sql
SELECT * FROM orders
RIGHT JOIN customers ON orders.customer_id = customers.id;
```

> Returns all customers and the matching orders; if no match, shows nulls for order info.

### 6. FULL (OUTER) JOIN

```sql
SELECT * FROM customers
FULL OUTER JOIN orders ON customers.id = orders.customer_id;
```

> Returns all customers and all orders, matching where possible, showing nulls otherwise.

Note: Not all databases support FULL OUTER JOIN.

---

## GROUP BY

**What it is:** Groups rows that have the same values into summary rows.

**What it does:** Often used with aggregation functions like COUNT(), AVG(), MAX(), etc.

**Example:**

```sql
SELECT country, COUNT(*)
FROM customers
GROUP BY country;
```

> Returns the number of customers per country.

---

## COMPOUND SELECT
We can use more than one SELECT statement to get the needed information, like setting up a query that relies on the result of another query
```sql
SELECT last_name, age
FROM students
WHERE age = (SELECT MAX (age) FROM students);
```
> This returns the oldest student(s).