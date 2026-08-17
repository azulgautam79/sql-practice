# SQL Practice — Lesson 4: Filtering and Sorting Query results

## SQL Syntax

```sql
SELECT DISTINCT column, another_column, ...
FROM myTable
WHERE condition(s)
    AND/OR another_condition
    AND/OR ...
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;
```

``` sql
    DISTINCT = removes duplicate rows
```
---

# SQL Lesson 4: Filtering and sorting query results

### 1. List all directors of Pixar movies (alphabetically), without duplicates

```sql
SELECT DISTINCT director FROM movies
ORDER BY director ASC;
```

### 2. List the last four Pixar movies released (ordered from most recent to least)

```sql
SELECT * FROM movies
ORDER BY YEAR DESC
LIMIT 4;
```

### 3. List the first five Pixar movies sorted alphabetically

```sql
SELECT * FROM movies
ORDER BY Title ASC
LIMIT 5;
```

### 4. List the next five Pixar movies sorted alphabetically

```sql
SELECT * FROM movies
ORDER BY Title ASC
LIMIT 5 OFFSET 5;
```

