# CS 341 (CSE341) — Database Systems (Fall 2024)

Repository archive for **CS 341 / CSE341: Database Systems** taught at the **Institute of Business Administration (IBA), Karachi, Pakistan** in **Fall 2024**.      
Instructor: **Abeera Tariq**

This repository is organized as a complete semester bundle containing:
- **Lab work (Oracle SQL, PL/SQL, ERD design, transactions/concurrency, MongoDB)**
- **Lecture slides (PDFs)**
- **Handwritten class notes (scanned/handwritten PDFs)**
- **Quizzes**
- **Reference books**

Each lab folder contains its own dedicated `README.md` explaining objectives, files, and how to run.

---

## What Was Covered in This Course

CS 341 builds a strong foundation in database systems, moving from conceptual modeling to practical querying and modern database tooling. The coverage in this repository includes:

### 1) Database Fundamentals & Design
- Database concepts, schemas, and real-world data modeling
- **ER modeling** (Chen + Crow’s Foot)
- Converting ERD → relational schema (PK/FK mapping)
- Integrity constraints and schema design

### 2) Relational Databases & SQL (Oracle)
- SQL querying from basics to advanced:
  - filtering, projection, sorting
  - aggregation & grouping (`GROUP BY`, `HAVING`)
  - built-in functions (string, numeric, date)
  - **joins** (inner/outer/self joins and different join syntaxes)
  - subqueries, correlated subqueries, `EXISTS/NOT EXISTS`
  - set operators (`UNION`, `INTERSECT`, `MINUS`)
  - views and reusable query logic
- **DDL** (schema creation and evolution): `CREATE`, `ALTER`, constraints, referential integrity
- **DML**: `INSERT`, `UPDATE`, `DELETE` with safe practices

### 3) PL/SQL (Oracle Procedural SQL)
- Procedures, conditionals, loops
- Cursors (explicit and implicit)
- Exception handling and robust program flow
- Modular programming patterns (e.g., packages / structured procedures)

### 4) Transactions & Concurrency (Oracle)
- Autocommit behavior and transaction boundaries
- `COMMIT`, `ROLLBACK`, `SAVEPOINT`
- Concurrency behavior across sessions
- Deadlocks and prevention strategies (e.g., row locks with `SELECT ... FOR UPDATE`)
- Isolation behavior (e.g., `READ COMMITTED`) and blocking/waiting semantics

### 5) NoSQL & MongoDB
- MongoDB environment setup (local/cloud)
- Importing datasets (JSON/CSV) into collections
- CRUD queries: filtering, projection, sorting, limiting
- Nested fields and arrays
- Aggregation pipelines for analytics-style outputs

---

## Repository Structure

High-level folders included in this repository:

- `books/`  
  Reference textbooks used during the semester.

- `lectures/`  
  Lecture slides (PDFs) covering theory + examples across the semester.

- `class-notes/`  
  Handwritten/scanned class notes for quick revision (uploaded as PDFs/images).

- `labs/`  
  All lab work (instructions + solution scripts + lab-specific readmes).

- `quizzes/`  
  Quiz PDFs and related materials.

- `Fall24Outline_CS341_Database Systems.pdf`  
  Official course outline/syllabus (Fall 2024).

---

## Lab Index (What Each Lab Covers)

Each lab has:
- its own folder under `labs/`
- a dedicated `README.md` inside the lab folder
- solution files (SQL scripts / ERDs / reports) as applicable

**Lab 01 — Intro to Oracle + HR Schema + Basic SQL**  
Lab 1 focuses on setting up the Oracle environment and practicing foundational SQL on the HR sample schema. It covers Oracle 19c/21c installation and SQL Developer setup, creating a new schema user via SQL*Plus, importing the HR schema script, and validating the setup by running basic SELECT queries. After setup, the lab introduces core SQL querying with WHERE filters, logical/comparison operators, range conditions (IN/BETWEEN), pattern matching (LIKE), and sorting (ORDER BY) through a set of practice questions executed on the HR tables (with LiveSQL as a fallback if local Oracle setup isn’t ready).

**Lab 02 — SQL Aggregations + SQL Functions**  
Lab 02 expands SQL practice on the HR schema by covering both aggregation and single-row functions. In Part A, it focuses on grouping and summarization using GROUP BY, HAVING, and aggregate functions (COUNT, SUM, AVG, MIN, MAX, DISTINCT) to answer department/job/location-level questions (including filtering aggregated results and working with NULLs). In Part B, it introduces SQL functions for formatting and transforming data—case conversion and string manipulation (UPPER/LOWER/INITCAP, SUBSTR, INSTR, LPAD/RPAD, TRIM, REPLACE), numeric functions (ROUND, TRUNC, MOD), and date operations (MONTHS_BETWEEN, ADD_MONTHS, NEXT_DAY, LAST_DAY, SYSDATE, TO_CHAR)—with a complete set of solved query scripts and demo slides.

**Lab 03 — DDL + Constraints + Insertions**  
Lab 03 introduces SQL Data Definition Language (DDL) and focuses on creating a fresh schema user and building database structure from scratch. It covers creating tables with appropriate data types, applying constraints (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY, CHECK) at both column and table level, creating tables using subqueries (where applicable), and performing schema evolution using ALTER TABLE. The lab then moves into insertion practice by building a small e-commerce style schema (Suppliers, Categories, Products, Orders, Order_Details), enforcing referential integrity and business rules (e.g., restricting invalid cities, disallowing quantity > 50, checking date format and later converting to DATE with TO_DATE), and implementing identity/auto-increment primary keys with default values like SYSDATE.

**Lab 04 — ERD Design (Chen + Crow’s Foot + DB Designer)**  
Lab 04 focuses on ERD design and translating requirements into a clean relational model. The lab practices modeling in multiple notations (Chen’s and Crow’s Foot) and then implementing the final design using DB Designer by defining entities, attributes, primary/foreign keys, and relationship cardinalities. It includes three scenarios: a university enrollment system (courses, offerings, students, instructors, enrollments and prerequisites), a cricket tournament system (countries/teams, players, matches, stadiums, umpires, and per-match player performance), and a hotel management system (rooms, floors, dining halls, room categories, occupancy types, pricing, and facilities), with final ERDs and exported SQL scripts for implementation.

**Lab 05 — SQL Joins (HR Schema)**  
Lab 05 (Joins) focuses on mastering SQL joins using the Oracle HR schema. In this lab, I practiced writing equivalent join queries using different approaches (Cartesian product + WHERE, JOIN ... USING, JOIN ... ON, and NATURAL JOIN) and compared their outputs, then moved on to real-world multi-table reporting tasks like employee–department–location details, job titles, self-joins for manager relationships, outer joins to include missing departments/managers, and analytical join queries such as “departments with no employees,” “employees earning more than their managers,” and aggregations like average salary per department and employee counts per job title.

**Lab 06 — Advanced SQL (Subqueries, CTEs, EXISTS, Views, Set Ops, CASE, DML)**  
Lab 06 focuses on advanced SQL querying and data manipulation using the Oracle HR schema. It covers nested and correlated subqueries, Common Table Expressions (CTEs) using the WITH clause, EXISTS/NOT EXISTS patterns, set operators (UNION, INTERSECT, MINUS), and conditional output using CASE. The lab also introduces view creation for reusable query logic and includes practical UPDATE and DELETE operations, followed by business-oriented reporting queries such as long-tenure employee lists and department-wise summary statistics.

**Lab 07 — Oracle-Backed Application (CRUD via REST)**  
Lab 07 (App Development with Oracle Database) introduces full-stack web application development using an Oracle Database as the data layer. It provides a compact OLTP Employee-Management System built on the HR schema and demonstrates end-to-end CRUD operations through REST APIs, including how the frontend communicates with a Node.js/Express backend, and how the backend executes SQL against Oracle. The lab emphasizes API testing using Postman, environment-based configuration using `.env` (with `.env.sample` provided instead of committing credentials), and the MVC (Model–View–Controller) architecture to separate routing, controller logic, and database-access models.

**Lab 08 — Intro to PL/SQL**  
Lab 08 (Intro to PL/SQL) introduces core PL/SQL programming concepts on Oracle using the HR schema. The lab covers building PL/SQL procedures, applying conditionals and loops, working with cursors, and integrating SQL inside PL/SQL using `SELECT ... INTO`. It includes procedural tasks such as printing number sequences and multiplication tables, parameterized procedures to retrieve employee email and city with error handling, cursor-based procedures to report department/job details, and data modification programs for salary swapping, conditional salary/commission updates, and safe employee deletion with referenced-table updates.

**Lab 09 — PL/SQL II**  
Lab 09 (PL/SQL II) extends procedural programming in Oracle by focusing on more advanced PL/SQL constructs and database programming patterns. The lab emphasizes writing robust stored procedures and logic using explicit/implicit cursors, loops, conditionals, exception handling, and parameterized routines that interact with HR schema tables. It includes cursor-driven reporting and validation tasks, safe update/delete workflows, and modularized PL/SQL solutions designed for reusability and correctness when working with real relational data. 

**Lab 10 — Transactions & Concurrency**  
Lab 10 (Transactions & Concurrency) demonstrates transaction management and concurrency control in Oracle using two simultaneous SQL*Plus sessions. The lab covers disabling autocommit, visibility of uncommitted changes, `COMMIT` vs `ROLLBACK`, partial rollbacks via `SAVEPOINT`, and the importance of committing only after completing a multi-statement operation to preserve atomicity. It also simulates a deadlock (ORA-00060), introduces `SELECT ... FOR UPDATE` to prevent deadlocks by locking rows up front, illustrates the lost update problem when concurrent updates overwrite each other, and applies the `READ COMMITTED` isolation level to observe blocking/waiting behavior during concurrent transactions.

**Lab 11 — Last of SQL (DCL + Advanced SQL/PLSQL)**  
Lab 11 (Last of SQL) consolidates database administration and advanced SQL/PL/SQL concepts by practicing Data Control Language (DCL) operations and modular PL/SQL programming. The lab includes creating and managing users, resetting/unlocking accounts, granting/revoking system and object privileges, creating roles, and verifying privileges through DBA views. It also revisits advanced query composition using the `WITH` clause (CTEs) and extends PL/SQL by building reusable database logic via packages (e.g., creating an `emp_manager` package to group procedures and executing packaged procedures for testing). 

**Lab 12 — MongoDB Setup + Intro to MongoDB**  
Lab 12 (MongoDB Setup + Intro to MongoDB) introduces NoSQL database fundamentals using MongoDB and covers both environment setup and core CRUD operations. It includes configuring MongoDB (local or cloud), connecting through MongoDB tools, importing JSON datasets into collections, and running essential document queries. The lab practices MongoDB query syntax for filtering, projection, sorting, and limiting results; updating and deleting documents; and working with nested fields and arrays through real datasets (e.g., restaurant documents), emphasizing how document-based modeling differs from relational SQL design. 

**Lab 13 — MongoDB II (Advanced Queries + Aggregation)**  
Lab 13 (MongoDB II) advances MongoDB skills by practicing more complex querying and data processing workflows on real datasets. It emphasizes working with larger/realistic collections (including importing structured datasets such as CSV), writing advanced queries with compound filters, sorting/limiting, and field projections, and applying aggregation pipelines (`$match`, `$group`, `$sort`, `$project`) to generate analytics-style outputs from document data. The lab reinforces best practices for handling semi-structured data in MongoDB and preparing query results suitable for reporting. 

---

## Notes on Running SQL/PLSQL Labs

- Most SQL labs use the **Oracle HR schema**.
- PL/SQL labs may use a dedicated schema user for clean execution.
- Transaction/concurrency labs require **multiple sessions** (e.g., two SQL*Plus windows) for correct simulation.

---

## Academic Integrity

This repository is intended as a structured academic archive for learning and revision. Any reuse must follow institutional academic integrity guidelines.
