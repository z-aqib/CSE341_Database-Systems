# Lab 09 — PL/SQL II (Advanced PL/SQL Programming)

## Overview
Lab 09 builds on introductory PL/SQL by practicing advanced database-programming techniques in Oracle. The lab focuses on writing structured and reusable PL/SQL code that integrates SQL queries and DML operations with procedural logic.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Learning Objectives
- Write parameterized PL/SQL procedures/functions for reusable logic
- Use loops and conditional control-flow for multi-step processing
- Use cursors (explicit/implicit) for row-by-row processing when required
- Apply exception handling to make programs robust and safe
- Perform controlled DML (UPDATE/DELETE) using validation logic and correct transactional behavior

## Contents
- `Lab09 - PL_SQL II.pdf` — official lab instructions
- `LAB9_zuha_aqib_26106.sql` — submitted solution script
- `Lab09_FarahInayat_26912.sql` — reference/alternate solution script (peer submission, included for comparison)

## Requirements
- Oracle Database with HR schema tables accessible (same schema used in earlier PL/SQL labs)
- Oracle SQL Developer (recommended) or SQL*Plus

## Setup Notes
For a clean run, this lab may be executed on a dedicated schema/user (as shown in local SQL*Plus user creation and SQL Developer connection screenshots). Do not commit any real passwords or credential screenshots to public repositories; keep passwords redacted.

## How to Run
### Option A — SQL Developer
1. Open Oracle SQL Developer and connect to the lab schema.
2. Open `LAB9_zuha_aqib_26106.sql`.
3. Run blocks in order (recommended to execute procedure definitions first, then test calls).

### Option B — SQL*Plus
1. Connect to the database:
   ```sql
   sqlplus username/password
    ```

2. Execute the script:

   ```sql
   @LAB9_zuha_aqib_26106.sql
   ```

## Notes

* Some PL/SQL scripts may include DML. For repeatable testing, use a fresh schema state or undo changes between runs.
* Always verify expected behavior by checking affected rows and validating results through SELECT queries after execution.