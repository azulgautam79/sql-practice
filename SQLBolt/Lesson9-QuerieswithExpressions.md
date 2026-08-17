# SQL Practice — Lesson 9: Queries with expressions

## SQL Syntax

```sql
SELECT particle_speed / 2.0 AS half_particle_speed
FROM physics_data
WHERE ABS(particle_position) * 10.0 > 500;
```
---

# SQL Lesson 9: Queries with expressions

### 1. List all movies and their combined sales in millions of dollars

```sql
SELECT title, (domestic_sales + internation_sales) / 1000000
AS gross_sales_millions
FROM movies
    JOIN boxoffice
    ON movies.id = boxoffice.movie_id;
```

### 2. List all movies and their ratings in percent

```sql
SELECT title, rating * 10 AS rating_percent
FROM movies
    JOIN boxoffice
    ON movies.id = boxoffice.movie_id;
```

### 3. List all movies that were released on even number years

```sql
SELECT title, year
FROM movies
WHERE year % 2 = 0;
```



