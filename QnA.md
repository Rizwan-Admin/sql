### 1.Write sql query to get all the record count from the Sales.Customer table using ADVENTURE2019 database


![image](https://github.com/user-attachments/assets/0bcef2ba-fffd-4b60-9022-729749de1bdc)
To get the total count of records from the `Sales.Customer` table in the `AdventureWorks2019` database, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(*) AS TotalCustomerCount
FROM Sales.Customer;
```

This query will return the total number of records in the `Sales.Customer` table.

### 2.Write a query to get all the records from the person id column in Sales.Customer table using ADVENTURE2019 database

Hint:  Null values in the column are not counted


![image](https://github.com/user-attachments/assets/3adf64bf-8f5b-4329-872c-877973053037)

To retrieve all the records from the `PersonID` column in the `Sales.Customer` table where the values are not `NULL`, use the following query:

```sql
USE AdventureWorks2019;
GO

SELECT PersonID
FROM Sales.Customer
WHERE PersonID IS NOT NULL;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   This sets the context to the `AdventureWorks2019` database.

2. **`SELECT PersonID`**:  
   Retrieves only the `PersonID` column.

3. **`FROM Sales.Customer`**:  
   Specifies the `Sales.Customer` table as the data source.

4. **`WHERE PersonID IS NOT NULL`**:  
   Filters the results to only include rows where the `PersonID` is not `NULL`. This ensures that no missing values (NULLs) are included in the result.


   ### 3.Write a query to get all the record of card type from sales.CreditCard table, no value should be repeated

Hint: Use distinct with count

![image](https://github.com/user-attachments/assets/cc405dd7-4575-492a-be34-c6d4fb1c8fd0)

To retrieve all the unique values of `CardType` from the `Sales.CreditCard` table without repeating any values, and count how many distinct `CardType` records there are, you can use the `DISTINCT` keyword along with `COUNT()` like this:

```sql
USE AdventureWorks2019;
GO

SELECT DISTINCT CardType
FROM Sales.CreditCard;
```

If you want to count the number of distinct `CardType` values as well, you can write:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(DISTINCT CardType) AS DistinctCardTypes
FROM Sales.CreditCard;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT DISTINCT CardType`**:  
   Retrieves all unique `CardType` values from the `Sales.CreditCard` table, meaning no repeated values.

3. **`COUNT(DISTINCT CardType)`**:  
   Counts the number of unique `CardType` values in the table.

The first query lists the unique card types, and the second query counts how many distinct card types there are.



### 4.Write sql query to get all the record count of the title column from Person.Person table.
![image](https://github.com/user-attachments/assets/10eb9851-91c2-4889-b861-6883fe9e5809)

To get the count of all records from the `Title` column in the `Person.Person` table, including `NULL` values, use the following query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(Title) AS TitleCount
FROM Person.Person;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`COUNT(Title)`**:  
   Counts all non-`NULL` values in the `Title` column.

3. **`FROM Person.Person`**:  
   Specifies that the data is being retrieved from the `Person.Person` table.

If you want to count all records (including rows where `Title` is `NULL`), you would use:

```sql
SELECT COUNT(*) AS TotalCount
FROM Person.Person;
```

- This second query counts all rows, regardless of whether the `Title` column contains a `NULL` or not.

- ### 5.write sql query to get all the record count from middle name column of Person.Person table
  ![image](https://github.com/user-attachments/assets/d5b91647-e8d0-4316-81de-a9083fba8bbc)

  To get the count of all records from the `MiddleName` column in the `Person.Person` table, excluding `NULL` values, you can use the following query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(MiddleName) AS MiddleNameCount
FROM Person.Person;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`COUNT(MiddleName)`**:  
   Counts all non-`NULL` values in the `MiddleName` column.

3. **`FROM Person.Person`**:  
   Specifies the table from which to retrieve the data.

If you want to count all rows in the table (including those with `NULL` in the `MiddleName` column), you could use:

```sql
SELECT COUNT(*) AS TotalCount
FROM Person.Person;
```

This counts all rows regardless of the `MiddleName` value.




