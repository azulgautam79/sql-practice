# SQL Practice — Lesson 7: Outer Joins

## SQL Syntax

```sql
SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table 
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
```
---

# SQL Lesson 7: Outer Joins
    Inner Join = Combines intersection of both tables

### 1. Find the list of all buildings that have employees

```sql
SELECT DISTINCT building FROM employees;
```

### 2. Find the list of all buildings and their capacity

```sql
SELECT * FROM buildings;
```

### 3. List all buildings and the distinct employee roles in each building (including empty buildings)

```sql
SELECT DISTINCT building_name, role 
FROM buildings 
  LEFT JOIN employees
    ON building_name = building;
```


