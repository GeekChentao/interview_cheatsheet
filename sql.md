# PostgreSQL
`
```sql
COALESCE(value1, value2, ..., valueN)
```
returns the first non-NULL expression in a list. If all arguments are `NULL`, it returns `NULL`.

```sql
SUBSTRING(arg::varchar, start_idx(start by 1), end_idx)
```
return the substring of a value

```sql
TO_CHAR(arg_date, fmt)
```
convert the value to string in varchar in fmt format and return
