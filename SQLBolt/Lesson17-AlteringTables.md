# SQL Practice — Lesson 17: Altering Tables

## SQL Syntax
Adding Columns
```sql
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint
    DEFAULT default_value;
```

Removing Columns
```sql
ALTER TABLE mytable
DROP column_to_be_deleted;
```

Renaming the table
```sql
ALTER TABLE mytable
RENAME TO new_table_name;
```

---

# SQL Lesson 17: Altering Tables

### 1. Add a column named Aspect_ratio with a FLOAT data type to store the aspect-ratio each movie was released in.

```sql
ALTER TABLE movies
    ADD COLUMN aspect_ratio FLOAT DEFAULT 2.39;
```

### 2. Add another column named Language with a TEXT data type to store the language that the movie was released in. Ensure that the default for this language is English.

```sql
ALTER TABLE movies
ADD COLUMN language TEXT DEFAULT "English";
```
