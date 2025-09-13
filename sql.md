# PostgreSQL

`COALESCE()`
```sql
COALESCE(value1, value2, ..., valueN)
```
The `COALESCE()` function in PostgreSQL returns the **first non-NULL expression** in a list.  
If all arguments are `NULL`, it returns `NULL`.