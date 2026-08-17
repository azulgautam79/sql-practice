# SQL Practice — Lesson 11: Queries with aggregates (Pt. 2)

## SQL Syntax

```sql
SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
FROM mytable
WHERE condition
GROUP BY column
HAVING group_condition;
```
---

# SQL Lesson 11: Queries with aggregates (Pt. 2)

### 1. Find the number of Artists in the studio (without a HAVING clause)

```sql
SELECT COUNT(role), building
FROM employees
WHERE role LIKE "%Artist%";
```

### 2. Find the number of Employees of each role in the studio

```sql
SELECT role, COUNT(*)
FROM employees
GROUP BY role;
```

### 3. Find the total number of years employed by all Engineers

```sql
SELECT role, SUM(years_employed)
FROM employees
WHERE role LIKE "%Engineer%";
```



