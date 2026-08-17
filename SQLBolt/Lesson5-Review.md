# SQL Practice — Lesson 5: SELECT Queries Review

## SQL Syntax

```sql
SELECT DISTINCT column, another_column, ...
FROM myTable
WHERE condition(s)
    AND/OR another_condition
    AND/OR ...
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;
```

``` sql
    DISTINCT = removes duplicate rows
```
---

    Latitude = North to South,
    +90° → North Pole
        ↑
        |
    0°  → Equator
        |
        ↓
    -90°  → South Pole 
    (North Pole +90°, equator 0°, -90° Antratica)
    ASC: South to North, DESC: North to South

    Longitude = East to West
    West                 0°                 East
    ←────────────────────|────────────────────→
                    Prime Meridian
    -180° far west, 0° Prime Meridian, +180° Far east
    ASC: West to East, DESC: East to West

# SQL Lesson 5: SELECT Queries Review

### 1. List all the Canadian cities and their populations

```sql
SELECT City, Population FROM north_american_cities
WHERE Country = "Canada";
```

### 2. Order all the cities in the United States by their latitude from north to south

```sql
SELECT City FROM north_american_cities
WHERE Country = "United States"
ORDER BY Latitude DESC;
```

### 3. List all the cities west of Chicago, ordered from west to east

```sql
SELECT City, Longitude FROM north_american_cities
WHERE Longitude < -87.629798
ORDER BY Longitude ASC;
```

### 4. List the two largest cities in Mexico (by population)

```sql
SELECT city, population FROM north_american_cities
WHERE country LIKE "Mexico"
ORDER BY population DESC
LIMIT 2;
```

### 5. List the third and fourth largest cities (by population) in the United States and their population

```sql
SELECT city, population FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

