# SQL Practice — Lesson 6: Multi-table queries with JOINs

## SQL Syntax

```sql
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
```
---

# SQL Lesson 6: Multi-table queries with JOINs INNER Join 
    Inner Join = Combines intersection of both tables

### 1. Find the domestic and international sales for each movie

```sql
SELECT * FROM Movies
INNER JOIN BoxOffice    // Joins all columns
    ON Movies.Id = BoxOffice.Movie_id;
```

### 2. Show the sales numbers for each movie that did better internationally rather than domestically

```sql
SELECT title, domestic_sales, international_sales
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id
WHERE international_sales > domestic_sales;
```

### 3. List all the movies by their ratings in descending order

```sql
SELECT title
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id
ORDER BY rating DESC;
```


