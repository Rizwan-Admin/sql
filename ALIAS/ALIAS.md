In SQL, an **alias** is a temporary name for a column or table to make queries easier to read.

### Column Alias:
```sql
SELECT column_name AS alias_name
FROM table_name;
```
Example:
```sql
SELECT first_name AS Name
FROM employees;
```

### Table Alias:
```sql
SELECT alias_name.column_name
FROM table_name AS alias_name;
```
Example:
```sql
SELECT e.first_name
FROM employees AS e;
```
