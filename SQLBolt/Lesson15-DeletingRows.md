# SQL Practice — Lesson 15: Deleting Rows

## SQL Syntax

```sql
DELETE FROM mytable
WHERE condition;
```

---

# SQL Lesson 15: Deleting Rows

### 1. The database is getting too big, lets remove all movies that were released before 2005.

```sql
DELETE FROM movies
WHERE year < 2005
```

### 2. Andrew Stanton has also left the studio, so please remove all movies directed by him.

```sql
DELETE FROM movies
WHERE director = "Andrew Stanton";
```