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
* show table ddl
```sql
 \d my_cool_table
```

* show tables (public by default)
```sql
 \dt
```

* show tables across all schemas
```sql
\dt *.
```

* show tables specific schema
```sql
\dt boom.
```
or
```sql
SET search_path TO boom, public;
\dt

```

* \dn - show schemas


# Simple table creation

```sql
CREATE TABLE topics (
  id serial PRIMARY KEY,
  name VARCHAR (100) NOT NULL
);
```

# Search path
## Show search path
```sql
show search_path;
```
## Edit search path
```sql
SET search_path TO my_new_path, public;
```

# Restore Heroku backup locally
```bash
pg_restore --verbose --clean --no-acl --no-owner -h localhost -d db_name db.dump
```

# Upgrade MacOS
```bash
brew postgresql-upgrade-database
```
