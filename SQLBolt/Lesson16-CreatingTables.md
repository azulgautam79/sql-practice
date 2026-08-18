# SQL Practice — Lesson 16: Creating tables

## SQL Syntax

```sql
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);
```
---

# SQL Lesson 16: Creating tables

### 1. Create a new table named Database with the following columns:
    i. Name A string (text) describing the name of the database
    ii. Version: A number (floating point) of the latest version of this database
    iii. Download_count An integer count of the number of times this database was downloaded
Table has not constraints

```sql
CREATE TABLE Database (
    id INTEGER PRIMARY KEY,
    Name TEXT,
    Version FLOAT,
    Download_count INTEGER
);
```