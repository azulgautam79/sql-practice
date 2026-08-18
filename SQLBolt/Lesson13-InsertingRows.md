# SQL Practice — Lesson 13: Inserting Rows

## SQL Syntax

```sql
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
```

---

# SQL Lesson 13: Inserting Rows

### 1. Add the studio's new production, Toy Story 4 to the list of movies (you can use any director)

```sql
INSERT INTO movies
VALUES (4, "Toy Story 4", "Lemon Gautam", 2003, 92);
```

### 2. Toy Story 4 has been relased to critical acclaim. It had a rating of 8.7, and make 340 million domestically and 270 million internationally. Add the record to the BoxOffice table.

```sql
INSERT INTO boxoffice
VALUES (4, 8.7, 340000000, 270000000);
```
