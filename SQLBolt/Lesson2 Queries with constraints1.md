# SQL Practice — Lesson 2: SELECT Queries

## SQL Operators

|             Operator            | Condition                                            | SQL Example                     |
| :-----------------------------: | :--------------------------------------------------- | :------------------------------ |
| `=`, `!=`, `<`, `<=`, `>`, `>=` | Standard numerical operators                         | `col_name != 4`                 |
|        `BETWEEN … AND …`        | Number is within range of two values (inclusive)     | `col_name BETWEEN 1.5 AND 10.5` |
|      `NOT BETWEEN … AND …`      | Number is not within range of two values (inclusive) | `col_name NOT BETWEEN 1 AND 10` |
|             `IN (…)`            | Number exists in a list                              | `col_name IN (2, 4, 6)`         |
|           `NOT IN (…)`          | Number does not exist in a list                      | `col_name NOT IN (1, 3, 5)`     |

---

## SQL Syntax

```sql
SELECT column, another_column,...
FROM myTable
WHERE condition
    AND/OR another_condition
    AND/OR ...;
```

---

# SQL Lesson 2: SELECT Queries with constraints 1

### 1. Find the movie with a row id of 6

```sql
SELECT * FROM movies
WHERE Id = 6;
```

### 2. Find the movies released in the year between 2000 and 2010

```sql
SELECT * FROM movies
WHERE Year BETWEEN 2000 AND 2010;
```

### 3. Find movies not released in the years between 2000 and 2010

```sql
SELECT * FROM movies
WHERE Year NOT BETWEEN 2000 AND 2010;
```

### 4. Find the first 5 Pixar movies and their release year.

```sql
SELECT title, year FROM movies
WHERE year <= 2003;
```

