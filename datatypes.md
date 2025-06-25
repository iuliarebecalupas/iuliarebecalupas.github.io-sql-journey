---
title: 4. Data Types
nav_order: 4
---

## SQL Data Types: What They Are and Why They Matter

Every piece of data stored in a database — whether it's a name, a number, or a date — has a data type. Data types tell the database what kind of data to expect and how to handle it.

Just like in real life you wouldn’t mix up phone numbers with birthdays, in SQL you need to match your data to the correct type.

Why Data Types Matter

- Ensure data is stored efficiently

- Prevent invalid data (e.g., letters in a number field)

- Help the database optimize queries and comparisons

- Make sure calculations and sorting behave correctly

---
### SQL Data Types
- ### String

| Type | Description |
|------|-------------|
| CHAR(n) | Fixed-length text - The _n_ parameter specifies the column length in characters  - can be from 0 to 255. Default is 1|
| VARCHAR(n) | Variable-length text	-  (can contain letters, numbers, and special characters). The size parameter specifies the maximum string length in characters - can be from 0 to 65535|
| CHARACTER(n) | Same as CHAR | 
| CHARACTER VARYING(n) | Same as VARCHAR | |

- ### Binary

| Type | Description | Example |
|------|-------------|---------|
| BINARY(n) | Fixed-length binary data | Binary codes of fixed size |
| VARBINARY(n) | Variable-length binary data | Files or images in a byte format |
| BLOB |Large Binary Object — stores large data blobs | Profile pictures, documents, etc. |


- ### Temporal 

| Type | Description | Example |
|------|-------------|---------|
| DATE | Stores a calendar date | '2024-06-01' |
| TIME | Stores time of day | '13:45:00' |
|TIMESTAMP | Date + time, used for logs/audit tracking | '2024-06-01 13:45' |	
|INTERVAL | Represents a duration (diff between times) | '2 days 3 hours' |

- ### Numeric 

| Type | Description | Example |
|------|-------------|---------|
| BIGINT | A large integer | 9223372036854775807 |
| SMALLINT | A small integer | 32767 |
| INT | A medium integer | 43 |
| DECIMAL | Exact decimal, good for money - range of data can be represented exactly with precision| 19.99 |
| FLOAT | Approximate decimal, can lose precision | 19.98999977111816 |
| NUMERIC | Same as DECIMAL (exact precision) |
| REAL | Approximate floating-point number | 3.14 |

_Note!_ SMALLINT vs INT — __SMALLINT__ takes less space and can store smaller numbers, __INT__ takes more space and can store bigger numbers - what matters is the data capacity behind it.

- ### Special

| Type | Description |
|------|-------------|
| BOOLEAN | True and False values|
| NULL | It is not the same thing as _0_, _no_, _!=_, _not equal_. NULL represents the absence of a value. 