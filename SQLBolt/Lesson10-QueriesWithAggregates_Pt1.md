# SQL Practice — Lesson 10: Queries with aggregates (Pt. 1)

## SQL Syntax

```sql
SELECT particle_speed / 2.0 AS half_particle_speed
FROM physics_data
WHERE ABS(particle_position) * 10.0 > 500;
```
---

# SQL Lesson 10: Queries with aggregates (Pt. 1)

### 1. Find the longest time that an employee has been at the studio

```sql
SELECT name, MAX(years_employed) AS longest_serving
FROM employees;
```

### 2. For each role, find the average number of years employed by employees in that role

```sql
SELECT role, AVG(years_employed) AS Average_years_employed
FROM employees
GROUP BY roles;
```

### 3. Find the total number of employee years worked in each building

```sql
SELECT building, SUM(years_employed) AS employee_years
FROM employees
GROUP BY building;
```



