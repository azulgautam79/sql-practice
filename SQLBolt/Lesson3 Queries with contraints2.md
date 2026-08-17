# SQL Practice — Lesson 3: SELECT Queries

## SQL Operators

| Operator | Condition | Example |
| :---: | :--- | :--- |
| `=` | Case-sensitive exact string comparison (notice the single equals) | `col_name = "abc"` |
| `!=` or `<>` | Case-sensitive exact string inequality comparison | `col_name != "abcd"` |
| `LIKE` | Case-insensitive exact string comparison | `col_name LIKE "ABC"` |
| `NOT LIKE` | Case-insensitive exact string inequality comparison | `col_name NOT LIKE "ABCD"` |
| `%` | Used anywhere in a string to match a sequence of zero or more characters (only with `LIKE` or `NOT LIKE`) | `col_name LIKE "%AT%"`<br>Matches `"AT"`, `"ATTIC"`, `"CAT"`, or even `"BATS"` |
| `_` | Used anywhere in a string to match a single character (only with `LIKE` or `NOT LIKE`) | `col_name LIKE "AN_"`<br>Matches `"AND"`, but not `"AN"` |
| `IN (…)` | String exists in a list | `col_name IN ("A", "B", "C")` |
| `NOT IN (…)` | String does not exist in a list | `col_name NOT IN ("D", "E", "F")` |

---

## SQL Syntax

```sql
SELECT column, another_column, ...
FROM myTable
WHERE condition
    AND/OR another_condition
    AND/OR ...;
```

---

# SQL Lesson 3: SELECT Queries with contraints 2

### 1. Find all the Toy Story movies

```sql
SELECT * FROM movies
WHERE Title LIKE "%Toy Story%";
```

### 2. Find all the movies directed by John Lasseter

```sql
SELECT * FROM movies
WHERE Director = "John Lasseter";
```

### 3. Find all the movies (and director) not directed by John Lasseter

```sql
SELECT * FROM movies
WHERE Director != "John Lasseter";
```

### 4. Find all the WALL-* movies

```sql
SELECT * FROM movies
WHERE Title LIKE "%Wall-%";
```

