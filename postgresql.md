# get list of indices

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
