# SQL---Code

# 📘 SQL Commands & RDBMS Overview

This document provides a clear explanation of essential SQL commands, SQL operators, clauses, and key database concepts such as RDBMS, tables, and primary keys. It serves as a quick reference for beginners and anyone revising SQL fundamentals.

---

## 🟦 SQL Command Categories

SQL commands are divided into the following categories based on their functionality:

---

## 📂 **DDL – Data Definition Language**

| Command | Description |
|--------|-------------|
| `CREATE` | Creates a new table, view, or another object in the database. |
| `ALTER`  | Modifies an existing database object (e.g., table). |
| `DROP`   | Deletes an entire table, view, or another object from the database. |

---

## 🟩 **DML – Data Manipulation Language**

| Command | Description |
|--------|-------------|
| `INSERT` | Adds new records to a table. |
| `UPDATE` | Modifies existing records. |
| `DELETE` | Removes records from a table. |

---

## 🟧 **DCL – Data Control Language**

| Command | Description |
|--------|-------------|
| `GRANT`  | Gives privileges to a user. |
| `REVOKE` | Takes back privileges granted to a user. |

---

## 🟪 **DQL – Data Query Language**

| Command | Description |
|--------|-------------|
| `SELECT` | Retrieves specific records from one or more tables. |

---

# 🗄️ What is RDBMS?

**RDBMS (Relational Database Management System)** is a system based on E. F. Codd’s relational model.  
It forms the foundation of SQL and is used in modern database systems such as:

- MySQL  
- Oracle  
- MS SQL Server  
- IBM DB2  
- Microsoft Access  

---

# 📋 What is a Table?

A **table** in RDBMS is a collection of related data organized in rows and columns.  
Each **row** represents a record, and each **column** represents a field.

---

# 🔑 Primary Key

A **Primary Key** is a field (or combination of fields) that:

- Uniquely identifies each record  
- Cannot contain duplicate values  
- Cannot contain `NULL` values  

---

# 🔍 WHERE Clause

The **WHERE clause** is used to filter records in SQL.  
It specifies a condition that must be met for rows to be selected, updated, or deleted.

**Example:**
sql
SELECT * FROM customers WHERE id = 5;
# 🔣 SQL Operators
➕ Arithmetic Operators
+, -, *, /, %

## 🔍 Comparison Operators
=   Equal to  
>   Greater than  
<   Less than  
>=  Greater than or equal to  
<=  Less than or equal to  
!= or <>  Not equal to

# ⚙️ Logical Operators
Operator	Description
AND	True when both conditions are true
OR	True when any one condition is true
NOT	Reverses the condition
📝 Important SQL Commands and Examples
# 🏗️ CREATE Command

Creates a table.

CREATE TABLE customers (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

# ➕ INSERT Command

Adds a new record.

INSERT INTO customers (id, name, email)
VALUES (1, 'John Doe', 'john@example.com');

# ✏️ UPDATE Command

Modifies an existing record.

UPDATE customers
SET email = 'newmail@example.com'
WHERE id = 1;

# ❌ DELETE Command

Deletes specific records.

DELETE FROM customers WHERE id = 1;

🔎 SELECT With AND / OR Examples
SELECT * FROM customers
WHERE city = 'Delhi' AND age > 25;

SELECT * FROM customers
WHERE city = 'Mumbai' OR city = 'Pune';

# ⭐ Summary

This README provides a structured overview of:

SQL command types

WHERE clause usage

Logical and comparison operators

CRUD operations with examples

RDBMS and table concepts

Great for beginners and quick revision!  
