
---

# Introduction to the `TOP` Function in SQL Server

## What is the `TOP` Function?

The `TOP` function in SQL Server is used to limit the number of rows returned by a query. This is especially useful when working with large datasets, as it allows you to retrieve only a specific number of rows or a percentage of the rows in the result set.

### Why Use `TOP`?

- **Performance**: When you don’t need all rows, the `TOP` function helps improve query performance by returning only a subset.
- **Convenience**: Useful when analyzing, reporting, or debugging data.
- **Flexibility**: You can return a fixed number of rows or a percentage of rows.

## Basic Syntax
```sql
SELECT TOP (number) [columns]
FROM [table]
WHERE [condition];
```

- **number**: The number of rows you want to retrieve.
- **columns**: The specific columns you want to display in the result.
- **table**: The table from which you are selecting data.
- **condition**: (Optional) Criteria to filter the results.

## Examples of Using the `TOP` Function

### 1. Retrieve a Fixed Number of Rows

This query retrieves the top 5 rows from the `Employees` table:
```sql
SELECT TOP 5 * 
FROM Employees;
```

### 2. Retrieve a Percentage of Rows

You can also return a percentage of rows. This example retrieves the top 10% of rows:
```sql
SELECT TOP 10 PERCENT * 
FROM Employees;
```

### 3. Using `WITH TIES`

If there are rows that have the same value as the last row in your result set, you can use `WITH TIES` to include them. This example includes any employees with the same salary as the 5th employee:
```sql
SELECT TOP 5 WITH TIES * 
FROM Employees
ORDER BY Salary DESC;
```

## Key Points to Remember
- The `TOP` function limits the number of rows returned.
- Can be combined with `ORDER BY` to sort the data before limiting the results.
- Use `WITH TIES` to include rows that have the same values as the last row in the result set.

---

