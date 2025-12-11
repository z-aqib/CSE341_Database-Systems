# Lab 08 — Intro to PL/SQL (Oracle HR Schema)

## Overview
Lab 08 introduces foundational PL/SQL programming in Oracle using the HR schema. The lab focuses on writing procedures and implementing control-flow constructs (conditionals, loops), using cursors, and combining SQL with PL/SQL for retrieval and data modification tasks. 

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Objectives
This lab is designed to develop understanding and usage of:
- Procedures
- Conditionals
- Loops
- Cursors

## Contents
- `Lab08 - Intro to PL_SQL.pdf` — Official lab instructions and questions
- `LAB8_zuha_aqib_26106.sql` — Submitted PL/SQL solution script
- `practice_lab8.sql` — Practice/working file for incremental testing

## Environment Setup
- Create a fresh Oracle user for the lab and execute the HR schema script to initialize a clean HR database instance.
- Connect using Oracle SQL Developer (hostname, port, SID/service configured locally).

## How to Run
### Option A — Oracle SQL Developer
1. Open SQL Developer and connect to the lab user/schema.
2. Open `LAB8_zuha_aqib_26106.sql`.
3. Run statements in order (recommended to run procedure blocks and tests section-by-section).

### Option B — SQL*Plus
1. Connect to the database:
   ```sql
   sqlplus username/password
    ```

2. Run the script:

   ```sql
   @LAB8_zuha_aqib_26106.sql
   ```

## Task Coverage (High-Level)

### Loops & Conditionals

* Print multiples of 2 using a `FOR` loop (2…12)
* Print 20 to 10 in decreasing order
* Determine even/odd using `MOD`
* Generate a multiplication table using a `WHILE` loop 

### SQL Inside PL/SQL (`SELECT ... INTO`)

* Print the `first_name` for employee ID 100 in a specified output format
* Procedure `get_email(empID)` to print employee email
* Procedure `get_emp_city(empID)` to print employee city and handle invalid IDs with a suitable error 

### Cursors

* Cursor procedure (open–fetch–close) to print job title and employee name for the IT department
* Procedure `get_job_history` using cursors + loop to print employee name, job_id, and start_date for department 50 

### Update/Delete in PL/SQL

* Interchange salaries of employees 120 and 122
* Conditional salary increase for employee 115 using `CASE` (experience-based) and print affected row count (`SQL%ROWCOUNT`)
* Procedure `update_emp_commission` using `IF` rules for employee 152 (salary/experience-based commission assignment)
* Procedure `delete_employee(emp_id)` to delete an employee safely by updating referenced tables first (reassign managed entities to the employee’s manager), then removing the employee record 