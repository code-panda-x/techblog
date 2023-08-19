---
title: "Sql Cheatsheet"
date: 2023-08-19T11:18:36-05:00
draft: false
tags: ["SQL","Programming"]
categories: ["Programming Language"]
slug: "sql-cheatsheet"
subtitle: "Sql Cheatsheet"
description: "Sql Cheatsheet"
keywords: 
- SQL
- Programming
- Gramma
---

#### SQL queries

SQL Summary: 
https://www.w3schools.com/sql/sql_examples.asp

SQL operations: 
https://www.w3schools.com/sql/sql_operators.asp


#### Select
```
select column from table
select distinct column from table

select distinct id from table

```

#### Where
```
SELECT * FROM Customers
WHERE Country='Mexico'

SELECT * FROM Customers
WHERE CustomerID=1

```

#### AND, OR and NOT Operators

```
SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München');

SELECT * FROM Customers
WHERE NOT Country='Germany' AND NOT Country='USA';

```

#### ORDER BY

This means that it orders by Country, but if some rows have the same Country, it orders them by CustomerName in descending order:

```
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;

```

#### IS NULL Operator

```
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;

SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;

```

#### SELECT TOP Clause
```
SELECT TOP 3 * FROM Customers;

SELECT * FROM Customers
LIMIT 3;
```

#### Functions
```
SELECT MIN(column_name)
```
Min()
Max()
Count()
Avg()
sum()

#### LIKE Operator
```
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```
The percent sign (%) represents zero, one, or multiple characters
The underscore sign (_) represents one, single character

Wildcard characters: https://www.w3schools.com/sql/sql_wildcards.asp

#### IN Operator
```
SELECT * FROM Customers
WHERE Country NOT IN ('Germany', 'France', 'UK');

SELECT * FROM Customers
WHERE Country IN (SELECT Country FROM Suppliers);
```

#### Between, Not Between
```
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20
AND CategoryID NOT IN (1,2,3);

SELECT * FROM Products
WHERE ProductName NOT BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni'
ORDER BY ProductName;
```

#### Joins
join xxx 
on xxx
```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

Different Types of SQL JOINs:
- (INNER) JOIN: Returns records that have matching values in both tables
- LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
- RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
- FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table

#### UNION Operator
The UNION operator is used to combine the result-set of two or more SELECT statements.
```
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```

#### GROUP BY 

Select number of customers from each country

```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
```

Group by: Basically Merge same records

#### HAVING
The HAVING clause was added to SQL because the **WHERE keyword cannot be used with aggregate functions**

```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
```

Combo: lists if the employees "Davolio" or "Fuller" have registered more than 25 orders:
```
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
WHERE LastName = 'Davolio' OR LastName = 'Fuller'
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 25;
```

Generally, select A, B, Group By A Having B

#### EXISTS 
The EXISTS operator is used to test for the existence of any record in a subquery.
```
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);
```

#### Comment
`--Select all`

#### Practice Problem

LC: 
1068: select columns from different tables, join
1581: count
197: comparsion
