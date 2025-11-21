# 🔗 SQL Joins — Complete Guide for Beginners

SQL Joins are used to **combine rows from two or more tables** based on a related column between them.  
They help in retrieving meaningful data spread across multiple tables in a relational database.

---

## 📌 Types of SQL Joins

| Join Type | Description | Returns |
|----------|-------------|---------|
| **INNER JOIN** | Matches rows with a common value in both tables | Matching records only |
| **LEFT JOIN** (Left Outer Join) | Returns all records from the left table + matching from the right | Unmatched rows from right become NULL |
| **RIGHT JOIN** (Right Outer Join) | Returns all records from the right table + matching from the left | Unmatched rows from left become NULL |
| **FULL OUTER JOIN** | Returns all matched + unmatched records from both tables | NULLs where data does not match |
| **CROSS JOIN** | Cartesian product: combines every row of A with every row of B | All possible combinations |
| **SELF JOIN** | A table joins with itself | Useful for hierarchical relationships |
| **NATURAL JOIN** | Automatically joins by columns with same name | Avoid ambiguity |

---

## 📍 1️⃣ INNER JOIN
Returns only rows where both tables have matching values.

sql
SELECT *
FROM TableA
INNER JOIN TableB
ON TableA.id = TableB.id;
🎯 Use: Fetch intersecting data only.

---

## 📍 2️⃣ LEFT JOIN (Left Outer Join)

Returns all rows from the left table and matched rows from the right.

SELECT *
FROM TableA
LEFT JOIN TableB
ON TableA.id = TableB.id;


📌 Unmatched right side becomes NULL.

---

## 📍 3️⃣ RIGHT JOIN (Right Outer Join)

Returns all rows from the right table and matched rows from the left.

SELECT *
FROM TableA
RIGHT JOIN TableB
ON TableA.id = TableB.id;


📌 Unmatched left side becomes NULL.

---

## 📍 4️⃣ FULL OUTER JOIN

Returns everything — matching and non-matching data from both tables.

SELECT *
FROM TableA
FULL OUTER JOIN TableB
ON TableA.id = TableB.id;


📌 NULLs where there is no matching data.

---

## 📍 5️⃣ CROSS JOIN

Returns a Cartesian Product, meaning every row of A joins with every row of B.

SELECT *
FROM TableA
CROSS JOIN TableB;


⚠️ Be careful — huge data output if tables are large.

---

## 📍 6️⃣ SELF JOIN

A table joins with itself.

SELECT A.name, B.name
FROM Employees A
INNER JOIN Employees B
ON A.manager_id = B.emp_id;


🎯 Useful for hierarchical queries (e.g., manager vs employee)

---

## 📍 7️⃣ NATURAL JOIN

Join automatically based on same column names in both tables.

SELECT *
FROM TableA
NATURAL JOIN TableB;


⚠️ Risky if unintended column matches occur.


---

## 🔍 Visual Summary
INNER JOIN → Only matches  
LEFT JOIN → All Left + Matches  
RIGHT JOIN → All Right + Matches  
FULL JOIN → All Left + All Right  
CROSS JOIN → Every combination  
SELF JOIN → Join table with itself  
NATURAL JOIN → Auto join on identical columns  

---
