---
title: SQL Basics
nav order: 1
---

# SQL Basics

Welcome to the starting point of learning SQL!  
This chapter introduces the key concepts you need to understand before writing any SQL code.

---

## What is SQL?

**SQL** stands for **Structured Query Language**.  
It is the standard language used to **communicate with relational databases**.  
With SQL, you can:

- Retrieve data from a database
- Insert new data or remove existing data
- Update or delete existing data
- Create or change the structure of database objects (like tables)

---

## Why Do We Need SQL?

Humans and computers don’t speak the same language.

When we ask questions like:

> _“Can you show me all customers who placed an order in the last week?”_

...a human understands this easily. But a machine doesn’t.

Computers need **clear**, **precise**, and **structured instructions** to fetch the right data.

This is where **SQL** comes in.

SQL gives us a way to **translate our questions into a format** the database can understand.

---

## What is a Database?

A **database** is a **collection of organized data** that can be easily accessed, managed, and updated.

Imagine an Excel file with multiple sheets, rows, and columns — a database is like that, but more powerful and designed for large-scale, structured data.

A database typically contains:

- **Tables** (like spreadsheets)
- **Rows** (each row is a record)
- **Columns** (each column is a field or attribute)
- Relationships between data (especially in *relational databases*)
  
  *Column(field)*
  ⬇️

<div style="display: flex; align-items: flex-start; gap: 16px;">
  <div>
  
| Name  | City   | Color  |
|-------|--------|--------|
| Jules | Paris  | Teal   |
| Alex  | Rome   | Yellow |
| James | London | Red    |

  </div>
  <div>
    ⬅️ <em>Row (record)</em>
  </div>
</div>

---

| Name | City | Color |
|------|------|-------|
| Jules | Paris | Teal |
| Alex | Rome | Yellow |
| James | London | Red |    ⬅️ *Row (record)*