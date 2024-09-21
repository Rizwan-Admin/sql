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


###  6. Formulate a SQL query to retrieve the total number of records present in the Sales.SalesPerson table.

![image](https://github.com/user-attachments/assets/c170517b-ad91-40e7-b370-591e6e991467)

To retrieve the total number of records present in the `Sales.SalesPerson` table, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(*) AS TotalSalesPersons
FROM Sales.SalesPerson;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT COUNT(*)`**:  
   Counts all the rows in the `Sales.SalesPerson` table, regardless of the values in the columns.

3. **`AS TotalSalesPersons`**:  
   Gives the count result a meaningful name, `TotalSalesPersons`.

4. **`FROM Sales.SalesPerson;`**:  
   Specifies that you are counting rows from the `Sales.SalesPerson` table.


   ### 7. Write an SQL query to determine the count of distinct country region codes present in the ‘SalesTerritory’ table.

   ![image](https://github.com/user-attachments/assets/cdb239c7-1133-42ee-8e38-86ab44aab97d)

   To determine the count of distinct `CountryRegionCode` values in the `Sales.SalesTerritory` table, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(DISTINCT CountryRegionCode) AS DistinctCountryRegionCodes
FROM Sales.SalesTerritory;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT COUNT(DISTINCT CountryRegionCode)`**:  
   Counts the number of unique (distinct) `CountryRegionCode` values in the `SalesTerritory` table.

3. **`AS DistinctCountryRegionCodes`**:  
   Assigns a meaningful alias to the result, `DistinctCountryRegionCodes`.

4. **`FROM Sales.SalesTerritory;`**:  
   Specifies that the data is being retrieved from the `Sales.SalesTerritory` table.


### 8. Write an SQL query to determine the count of distinct currency codes present in the ‘CurrencyRate’ table.

![image](https://github.com/user-attachments/assets/f0709ff9-5d94-40af-9a9b-6a052325df90)

To determine the count of distinct currency codes in the `Sales.CurrencyRate` table, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(DISTINCT ToCurrencyCode) AS DistinctCurrencyCodes
FROM Sales.CurrencyRate;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT COUNT(DISTINCT ToCurrencyCode)`**:  
   Counts the number of unique (distinct) values in the `ToCurrencyCode` column of the `Sales.CurrencyRate` table.

3. **`AS DistinctCurrencyCodes`**:  
   Assigns a meaningful alias, `DistinctCurrencyCodes`, to the result.

4. **`FROM Sales.CurrencyRate;`**:  
   Specifies that the data is being retrieved from the `Sales.CurrencyRate` table. 

If you also want to check distinct values for `FromCurrencyCode`, you can adjust the column name.


### 9. Write an SQL query to calculate the count of email addresses that were last modified before December 22, 2008, grouped by the modification date, but only include those modification dates where the count of email addresses is greater than 1.

![image](https://github.com/user-attachments/assets/e81d31e2-f441-4575-9c1d-2cb0fd6cd788)

To calculate the count of email addresses that were last modified before December 22, 2008, and group them by modification date, including only those dates where the count of email addresses is greater than 1, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT ModifiedDate, COUNT(EmailAddress) AS EmailCount
FROM Person.EmailAddress
WHERE ModifiedDate < '2008-12-22'
GROUP BY ModifiedDate
HAVING COUNT(EmailAddress) > 1;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT ModifiedDate, COUNT(EmailAddress) AS EmailCount`**:  
   - Selects the `ModifiedDate` and counts the number of email addresses for each modification date.
   - `COUNT(EmailAddress)` returns the number of email addresses grouped by modification date.

3. **`FROM Person.EmailAddress`**:  
   Specifies that data is being retrieved from the `Person.EmailAddress` table.

4. **`WHERE ModifiedDate < '2008-12-22'`**:  
   Filters records to include only those where the `ModifiedDate` is before December 22, 2008.

5. **`GROUP BY ModifiedDate`**:  
   Groups the results by `ModifiedDate`.

6. **`HAVING COUNT(EmailAddress) > 1`**:  
   Filters the results to include only those `ModifiedDate` values where the count of email addresses is greater than 1. This ensures that only dates with more than one email modification are shown.


   ### 10. Write an SQL query to calculate the count of sales orders where the CreditCardID is greater than 10000.

![image](https://github.com/user-attachments/assets/f6dae5df-a47e-49e6-9dc8-d3d0a625e9a7)



To calculate the count of sales orders where the `CreditCardID` is greater than 10,000, you can use the following SQL query:

```sql
USE AdventureWorks2019;
GO

SELECT COUNT(*) AS SalesOrderCount
FROM Sales.SalesOrderHeader
WHERE CreditCardID > 10000;
```

### Explanation:
1. **`USE AdventureWorks2019;`**:  
   Sets the context to the `AdventureWorks2019` database.

2. **`SELECT COUNT(*)`**:  
   Counts the total number of sales orders that meet the condition.

3. **`AS SalesOrderCount`**:  
   Assigns an alias (`SalesOrderCount`) to the result.

4. **`FROM Sales.SalesOrderHeader`**:  
   Specifies the `Sales.SalesOrderHeader` table as the data source.

5. **`WHERE CreditCardID > 10000`**:  
   Filters the rows to include only those records where the `CreditCardID` is greater than 10,000.




