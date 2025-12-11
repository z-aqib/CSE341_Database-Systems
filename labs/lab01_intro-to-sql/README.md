# Lab 01 — Oracle Setup + Intro to SQL (HR Schema)

This lab covers two parts:
1) **Oracle + SQL Developer setup and HR schema initialization** (Lab01A)  
2) **Introductory SQL querying practice** using the HR schema (Lab01B)

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Learning Objectives

### Part A — Environment Setup
- Install Oracle **19c/21c** and Oracle **SQL Developer**
- Create a database user and run the **HR schema** setup script

### Part B — SQL Fundamentals
Practice basic SQL queries using:
- `SELECT` + `WHERE`
- Logical & comparison operators
- `IN`, `NOT IN`, `BETWEEN`
- `LIKE` (wildcards)
- `ORDER BY` sorting

---

## Contents of This Folder

Files included in this lab folder: 
- `Lab01A - Installation of Oracle and HR Database Setup.pdf` — setup guide
- `Lab01B - Intro to SQL.pdf` — tasks + submission requirements
- `Lab01Demo_Intro to SQL.pdf` — lecture/demo slides
- `hr_schema.sql` — HR sample schema objects + data (used for LiveSQL / schema setup)
- `LAB1.sql` — quick practice file
- `LAB1_zuhaaqib_26106.sql` — solved queries (with question-wise comments)
- `testdb.sql` — small custom table + inserts for quick testing

---

## Setup Options

### Option 1 (Recommended): Local Oracle + SQL Developer
The lab guide walks through installation and then creating a schema user using SQL*Plus:

- Connect as SYSDBA:
  - `sqlplus / as sysdba`
- Create a user (Oracle common user style with `c##` prefix) and grant privileges:
  - `CREATE USER c##... IDENTIFIED BY ...;`
  - `GRANT UNLIMITED TABLESPACE ...;`
  - `GRANT CONNECT, RESOURCE, DBA ...;`

Then connect through SQL Developer by creating a new connection and using the correct **service name/SID** (commonly `orcl`). 

Finally, execute the provided HR schema script to create the tables and data.

---

### Option 2 (Fallback): Oracle LiveSQL (if local setup isn’t ready)
If you face setup issues, the lab allows you to use **LiveSQL** and select the **Human Resources (HR)** schema:

Note: On LiveSQL, HR tables are accessed with the `HR.` prefix (e.g., `HR.EMPLOYEES`).

---

## What to Run

1) **(If needed) Create HR schema objects/data**
- Run `hr_schema.sql` (used to generate the HR schema tables and sample data)

2) **Solve the SQL practice questions**
- Open and run: `LAB1_zuhaaqib_26106.sql`  
The tasks include queries on employees/jobs/hiring dates, salary filters, NULL checks, IN/BETWEEN/LIKE conditions, and sorting via ORDER BY.

---

## Notes
- Keep credentials local and avoid committing any real passwords/screenshots to public repos.
- SQL keywords are case-insensitive (formatting consistency still matters for readability). 