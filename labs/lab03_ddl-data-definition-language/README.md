# Lab 03 — DDL (Create/Alter/Drop) + Constraints + Insertions

This lab focuses on **SQL Data Definition Language (DDL)** and creating a clean schema from scratch.
You create a new Oracle user (new schema), define tables with appropriate data types, enforce integrity
using constraints, evolve schemas using ALTER commands, and insert sample data to validate rules.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Learning Objectives

By the end of this lab, you should be able to:
- Create tables using `CREATE TABLE`
- Choose appropriate data types (e.g., `VARCHAR2`, `NUMBER`, `DATE`)
- Apply constraints:
  - `NOT NULL`, `UNIQUE`, `PRIMARY KEY`, `FOREIGN KEY`, `CHECK`, `DEFAULT`
- Use column-level vs table-level constraints
- Create tables using subqueries (where supported)
- Insert data and validate constraints
- Drop tables using `DROP TABLE`

---

## Files Included

- `Lab03 - Intro to DDL.pdf` — lab instructions + tasks
- `Lab03Demo_DDL.pdf` — lecture/demo slides for DDL + constraints
- `LAB3_zuhaaqib_26106.sql` — complete solution script (question-wise)

---

## Setup (New User / New Schema)

This lab uses a **new user** because you are creating a new schema. 
1. Create the user (via SQL*Plus as SYSDBA, or with lab engineer help if using lab PCs).
2. Connect to this user in **SQL Developer** and run your script file.
3. If Oracle/SQL Developer causes issues, you may use **LiveSQL** as backup.

---

## What You Build

### Part A — Create Tables + Constraints
You create tables like:
- `my_first_table` (basic datatypes) 
- `Products`, `Suppliers`, `Categories`, `Orders`, `Order_Details` 

You also enforce rules such as:
- “No NULLs” in required attributes 
- City must be one of allowed values (e.g., KHI/ISB/LHR) 
- Quantity must not exceed 50 (CHECK constraint) 
- Primary keys, foreign keys, unique constraints, and named constraints (recommended) 

DDL concepts are reinforced through the demo slides: constraints, ALTER operations, drop vs truncate,
identity/auto-increment, and default values.

---

### Part B — Insert Sample Data + Validation
You insert sample rows into:
- `Categories`, `Suppliers`, `Products` and then run recall queries to verify correctness. 

You also test:
- A strict date pattern as a string using LIKE (e.g., `__/__/____`) and then modify the column to `DATE`
  and use `TO_DATE` correctly for inserts. 
- Auto-increment primary key (IDENTITY) and default `SYSDATE` for order_date.

---

## How to Run (SQL Developer)

1. Open **Oracle SQL Developer**
2. Connect using your Lab 03 schema user
3. Open `LAB3_zuhaaqib_26106.sql`
4. Run section-by-section to verify:
   - tables created successfully
   - constraints behave correctly (expected failures on invalid inserts)
   - sample data inserts correctly
   - verification SELECT queries return expected rows

---

## Notes / Oracle Differences
- Some “CREATE IF NOT EXISTS” style statements and certain “duplicate structure” shortcuts may not work in Oracle
  (you can still write them as answers when the lab notes allow it).
- Prefer naming constraints (helps with future ALTER/DROP operations).
