# SQL Practice — Lesson 8: A short note on Nulls

## SQL Syntax

```sql
SELECT column, another_column, …
FROM mytable
WHERE column IS/IS NOT NULL
AND/OR another_condition
AND/OR …;
```
---

# SQL Lesson 8: A short note on Nulls

### 1. Find the name and role of all employees who have not been assigned to a building

```sql
SELECT name, role 
FROM employees 
WHERE building IS NULL;
```

### 2. Find the names of the buildings that hold no employees

```sql
SELECT DISTINCT building_name
FROM buildings
    LEFT JOIN employees
        ON building_name = building
    WHERE role IS NULL;
```



