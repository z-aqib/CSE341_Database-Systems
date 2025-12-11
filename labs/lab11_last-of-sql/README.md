# Lab 11 — Last of SQL (DCL + Advanced SQL/PL/SQL)

## Overview
Lab 11 consolidates core SQL skills with database administration and advanced PL/SQL concepts. The lab focuses on Data Control Language (DCL) workflows (user and privilege management), privilege verification using DBA views, and modular PL/SQL through packages.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Learning Objectives
- Perform DCL operations for user administration (create user, alter user, unlock/reset password).
- Grant and revoke system privileges and object privileges.
- Create roles, grant privileges to roles, and assign roles to users.
- Verify privilege assignments using relevant DBA views.
- Revisit advanced query structuring using the `WITH` clause (CTEs).
- Apply advanced PL/SQL organization using packages to group related procedures.

## Contents
- `Lab11 - Last of SQL.pdf` — official lab instructions and tasks
- `lab11_zuha_aqib_26106.sql` — submitted SQL/PLSQL solution script
- `lab11_zuha_aqib_26106.docx` — submission report (screenshots + explanations)
- `lab11_zuha_aqib_26106.pdf` — exported submission report (PDF)

## Requirements
- Oracle Database (local installation recommended for DCL tasks requiring SYSDBA access)
- SQL*Plus (required for command-line SYSDBA tasks) and/or Oracle SQL Developer
- HR schema access (for PL/SQL procedure/package testing, where applicable)

## Execution Notes
### Part A — DCL (Command Line / SYSDBA)
The DCL portion is executed in SQL*Plus as SYSDBA and includes:
- Creating a user and managing its password/status
- Granting system privileges (e.g., `CREATE SESSION`, `CREATE TABLE`)
- Creating a role and assigning privileges to it
- Granting the role to the user
- Granting and revoking object privileges on a table
- Verifying grants using DBA views (e.g., `DBA_USERS`, `DBA_ROLE_PRIVS`, `DBA_TAB_PRIVS`)

If required by the lab environment, session formatting commands may be used to improve output readability (e.g., LINESIZE/PAGESIZE and column formatting).

### Part B — Advanced SQL / PL/SQL (SQL Developer or LiveSQL)
The remainder of the lab may be completed using SQL Developer or LiveSQL, depending on environment constraints.
A key task includes building a package (e.g., `emp_manager`) to group related procedures and then running packaged procedures to validate correct behavior.

## How to Run
### Option A — SQL Developer
1. Open SQL Developer and connect to the target schema.
2. Open `lab11_zuha_aqib_26106.sql`.
3. Execute statements in order:
   - DCL verification queries (if applicable to the session)
   - Table creation/inserts (if included)
   - Package creation
   - Procedure calls and test cases

### Option B — SQL*Plus
1. Connect as needed:
   - SYSDBA for DCL tasks
   - Lab user for table access and testing
2. Run the script:
   ```sql
   @lab11_zuha_aqib_26106.sql
    ```
