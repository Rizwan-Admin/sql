

# SQL Server `TOP` Function Cheat Sheet

## Overview
The `TOP` function in SQL Server is used to limit the number of rows returned in a query result set.

## Syntax
```sql
SELECT TOP (number) [columns]
FROM [table]
WHERE [condition];
```

- **number**: Number of rows to return.
- **columns**: Columns you want to retrieve.
- **table**: Table from which you retrieve data.
- **condition**: (Optional) Filters to refine the result set.

## Examples

### 1. Retrieve Top N Rows
Retrieve the top 5 rows from a table:
```sql
SELECT TOP 5 * 
FROM Employees;
```

### 2. Retrieve Top N Rows with Condition
Retrieve the top 10 highest-paid employees in the Sales department:
```sql
SELECT TOP 10 FirstName, LastName, Salary 
FROM Employees
WHERE Department = 'Sales'
ORDER BY Salary DESC;
```

### 3. Use `TOP` with Percentage
Return the top 10% of rows:
```sql
SELECT TOP 10 PERCENT * 
FROM Employees
ORDER BY HireDate ASC;
```

### 4. Use `TOP` with `WITH TIES`
Include tied rows when using the `ORDER BY` clause:
```sql
SELECT TOP 5 WITH TIES * 
FROM Employees
ORDER BY Salary DESC;
```

---

## Key Points
- The `TOP` function restricts the number of rows returned.
- Can be combined with `PERCENT` to retrieve a percentage of rows.
- Use `WITH TIES` to include rows that have equal values based on the `ORDER BY` clause.

---
