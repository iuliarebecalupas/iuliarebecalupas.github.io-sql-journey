---
title: SQL Statements: DML, DDL, and Query Structure
nav order: 1
---

## Understanding SQL Statements: DML, DDL, and Query Structure

Now that we understand what SQL is and why we use it, let's break down the two major roles SQL plays — and how statements are built.

##  Two Main Roles of SQL

SQL is used to either:

1. **Define the structure of the database** (DDL – Data Definition Language)
2. **Manipulate the data inside the database** (DML – Data Manipulation Language)

### 🔧 DDL (Data Definition Language)
DDL statements define or modify the structure of a database — such as creating or altering tables.

Examples:
- `CREATE` – make a new table
- `ALTER` – change the structure of a table
- `DROP` – delete a table or database

>  Think of DDL like setting up the walls and shelves of a library.

---

###  DML (Data Manipulation Language)
DML statements are used to work with the data inside the tables. This is where you perform CRUD operations:

- **C**reate → `INSERT`
- **R**ead → `SELECT`
- **U**pdate → `UPDATE`
- **D**elete → `DELETE`

>  In this guide, we’ll focus on **DML**, since it’s what we use to *query* and *work with* data.

A **query** is a specific type of SQL statement that retrieves data — usually using the `SELECT` command.

> All queries are SQL statements, but **not all SQL statements are queries**.

Some SQL statements change data or structure (like `UPDATE`, `CREATE`, or `DELETE`).  
A query just *asks* the database to return data.

---

##  A Few Key Things About SQL Statements

- **They are whitespace-independent**  
  You can write SQL in one line or break it into multiple lines for readability.

- **They end with a semicolon `;`**  
  This tells the database engine that your statement is complete.

- **They are made up of clauses**  
  A clause is like a building block of a statement — each one plays a role.

---

##  Understanding SQL Clauses (Building Blocks of Statements)

A **clause** is a part of an SQL statement that performs a specific role. Think of it like a sentence made of smaller parts — each one gives the database a piece of information about what you want to do.

An SQL statement is usually made up of multiple clauses. Sometimes, a single clause **can act as a full statement** if it's simple enough.

---

###  What Defines a Clause?

Each clause begins with a **keyword**, and may contain several other elements like field names, table names, conditions, and operators.

Here’s what each component means:

---

###  Components of a Clause

| Component      | What It Does                                                                 |
|----------------|------------------------------------------------------------------------------|
| **Keywords**   | Reserved words that tell the database to take a specific action. <br>Examples: `SELECT`, `FROM`, `WHERE`, `UPDATE`, `DELETE`, `INSERT`|
| **Field Names**| Names of the columns you want to work with.<br>Examples: `customer_name`, `price`, `order_date` |
| **Table Names**| Tell the database which table to pull data from.<br>Examples: `orders`, `users`, `products` |
| **Predicates** | Describe **conditions** that must be met for the action to happen.<br>They usually contain an *expression* (a value or formula to match).<br>Example: `price > 100` or `status = 'active'` |
| **Operators**  | Help compare or filter data.<br>Examples: `=`, `>`, `<`, `BETWEEN`, `LIKE`, `IN`, `IS NULL` |