# Get current db
```sql
SELECT current_database();
```

# Get list of indices

```sql
SELECT *
FROM pg_indexes
WHERE tablename NOT LIKE 'pg%';
```

or for a specific table

```sql
SELECT *
FROM pg_indexes
WHERE tablename = 'my_fancy_table';
```

# shortcuts
* \dt - show tables
* \dn - show schemas


# Simple table creation

```sql
CREATE TABLE topics (
  id serial PRIMARY KEY,
  name VARCHAR (100) NOT NULL
);
```
