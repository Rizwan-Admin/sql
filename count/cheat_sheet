Here’s a basic SQL `COUNT()` cheatsheet to help you understand and use different variations of the `COUNT()` function in SQL. This covers the most common ways to count rows and records in a database table.

---

### **Basic SQL `COUNT()` Syntax**
```sql
SELECT COUNT(*) 
FROM table_name;
```
- **Description**: Counts all rows in the table.

---

### **Counting Non-NULL Values in a Column**
```sql
SELECT COUNT(column_name)
FROM table_name;
```
- **Description**: Counts all non-NULL values in the specified column.

---

### **Counting with a Condition (Using `WHERE`)**
```sql
SELECT COUNT(*)
FROM table_name
WHERE condition;
```
- **Description**: Counts rows that satisfy a given condition in the `WHERE` clause.

---

### **Counting Distinct Values**
```sql
SELECT COUNT(DISTINCT column_name)
FROM table_name;
```
- **Description**: Counts unique (distinct) values in the specified column, ignoring duplicates.

---

### **Counting with `GROUP BY`**
```sql
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;
```
- **Description**: Counts rows for each distinct value in the column. Useful for categorizing counts (e.g., counting employees per department).

---

### **Counting with Multiple Conditions (Using `HAVING`)**
```sql
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > some_number;
```
- **Description**: Filters groups based on a condition. For example, count only groups with more than a certain number of records.

---

### **Counting with Multiple Columns**
```sql
SELECT COUNT(column1, column2)
FROM table_name;
```
- **Description**: Counts rows that contain non-NULL values in both `column1` and `column2`.

---

### **Count with Joins**
```sql
SELECT COUNT(*)
FROM table1
JOIN table2 ON table1.id = table2.id;
```
- **Description**: Counts rows after joining two tables based on a condition (e.g., counting records from a related table).

---

### Example Queries:

#### 1. **Total Number of Orders**
```sql
SELECT COUNT(*) AS TotalOrders
FROM Orders;
```

#### 2. **Count Non-NULL Email Addresses**
```sql
SELECT COUNT(Email) AS EmailCount
FROM Customers;
```

#### 3. **Count Orders per Customer**
```sql
SELECT CustomerID, COUNT(*) AS OrderCount
FROM Orders
GROUP BY CustomerID;
```

#### 4. **Count Distinct Product Categories**
```sql
SELECT COUNT(DISTINCT CategoryID) AS DistinctCategories
FROM Products;
```

#### 5. **Count Customers with More Than 5 Orders**
```sql
SELECT CustomerID, COUNT(*) AS OrderCount
FROM Orders
GROUP BY CustomerID
HAVING COUNT(*) > 5;
```

---

This cheatsheet provides the most common ways to use the `COUNT()` function in SQL. It's a handy guide to quickly look up how to count records in different scenarios.
