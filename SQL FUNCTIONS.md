# 🗄️ SQL Functions — Complete Guide for Beginners

SQL Functions are predefined operations that **use input values**, perform calculations or transformations, and **return a result**.  
They help in manipulating data and performing mathematical, string, date/time, and aggregate operations efficiently.

---

## 📌 Types of SQL Functions

SQL functions are mainly classified into two types:

| Type | Description | Example |
|------|-------------|---------|
| **Single Row Functions** | Operate on **one row at a time** and return **one result per row** | UPPER(), LENGTH(), ROUND() |
| **Multiple Row Functions** (Aggregate) | Operate on **multiple rows** and return **one result per group** | SUM(), AVG(), COUNT() |

---

## ✳️ 1️⃣ String Functions

| Function | Description | Example |
|---------|-------------|---------|
| `UPPER()` | Converts text to uppercase | `UPPER(name)` |
| `LOWER()` | Converts text to lowercase | `LOWER(city)` |
| `LENGTH()` | Returns length of string | `LENGTH('Hello') → 5` |
| `SUBSTR()` / `SUBSTRING()` | Extracts part of a string | `SUBSTR('Database', 1, 4) → 'Data'` |
| `CONCAT()` | Joins strings | `CONCAT(first_name, last_name)` |
| `TRIM()` | Removes spaces | `TRIM('  SQL ') → 'SQL'` |

---

## 🔢 2️⃣ Numerical Functions

| Function | Description | Example |
|---------|-------------|---------|
| `ROUND()` | Rounds number to given decimals | `ROUND(9.567, 2) → 9.57` |
| `ABS()` | Returns absolute value | `ABS(-45) → 45` |
| `CEIL()` | Rounds up | `CEIL(9.1) → 10` |
| `FLOOR()` | Rounds down | `FLOOR(9.9) → 9` |
| `MOD()` | Remainder after division | `MOD(10, 3) → 1` |

---

## 📅 3️⃣ Date & Time Functions

| Function | Description | Example |
|---------|-------------|---------|
| `CURRENT_DATE()` | Today's date | `2025-11-21` |
| `NOW()` | Current date & time | `2025-11-21 10:30:00` |
| `DATEDIFF()` | Difference between two dates | `DATEDIFF('2025-12-01','2025-11-21')` |
| `DATE_ADD()` | Adds days/months/years | `DATE_ADD(CURRENT_DATE(), INTERVAL 5 DAY)` |
| `EXTRACT()` | Extracts year/month etc. | `EXTRACT(YEAR FROM date_col)` |

---

## 📊 4️⃣ Aggregate Functions  
(*Used with GROUP BY*)

| Function | Description | Example |
|---------|-------------|---------|
| `COUNT()` | Number of records | `COUNT(*)` |
| `SUM()` | Total value | `SUM(salary)` |
| `AVG()` | Average value | `AVG(marks)` |
| `MAX()` | Highest value | `MAX(price)` |
| `MIN()` | Lowest value | `MIN(price)` |

---

## 🧠 5️⃣ Conversion Functions

| Function | Description | Example |
|---------|-------------|---------|
| `CAST()` | Converts data type | `CAST('100' AS INT)` |
| `CONVERT()` | Converts to another type | `CONVERT(INT, '50')` |
| `TO_DATE() / STR_TO_DATE()` | Converts string to date | `STR_TO_DATE('21-11-2025','%d-%m-%Y')` |

---

## 🧪 Example SQL Queries

```sql
SELECT 
    UPPER(name) AS Name_Upper,
    LENGTH(name) AS Name_Length,
    ROUND(salary, 2) AS Rounded_Salary,
    YEAR(joining_date) AS Joining_Year
FROM employees;
