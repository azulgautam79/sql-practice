# SQL Practice — Lesson 14: Updating Rows

## SQL Syntax

```sql
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;
```

---

# SQL Lesson 14: Updating Rows

### 1. The director for A Bug's Life is incorrect, it was actually directed by John Lasseter

```sql
UPDATE movies
SET director = "John Lasseter"
WHERE id = 4;
```

### 2. The year that Toy Story 2 was released is incorrect, it was actually released in 1999

```sql
UPDATE movies
SET year = 1999
WHERE id = 3;
```

### 3. Both the title and director for Toy Story 8 is incorrect! The title should be "Toy Story 3" and it was directed by Lee Unkrich

```sql
UPDATE movies
SET title = "Toy Story 3", director = "Lee Unkrich"
WHERE id = 11;
```