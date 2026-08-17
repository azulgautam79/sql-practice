# SQL Practice — Lesson 12: Order of Execution of a Query

## SQL Syntax

```sql
SELECT DISTINCT column, AGG_FUNC(column_or_expression), …
FROM mytable
    JOIN another_table
      ON mytable.column = another_table.column
    WHERE constraint_expression
    GROUP BY column
    HAVING constraint_expression
    ORDER BY column ASC/DESC
    LIMIT count OFFSET COUNT;
```
---

# SQL Lesson 12: Order of Execution of a Query

### 1. Find the number of movies each director has directed

```sql
SELECT director, COUNT(id) as Num_movies_directed
FROM movies
GROUP BY director;
```

### 2. Find the total domestic and international sales that can be attributed to each director

```sql
SELECT director, SUM(domestic_sales + international_sales) AS Cumulative_sales_from_all_movies
FROM movies
    INNER JOIN boxoffice
        ON movies.id = boxoffice.movie_id
    GROUP BY director;
```




