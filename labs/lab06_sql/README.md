# Lab 06 — SQL (Subqueries, CTEs, EXISTS, Views, Set Operators, CASE, UPDATE/DELETE)

## Overview
This lab practices advanced SQL constructs using the Oracle HR schema. The tasks include writing nested and correlated subqueries, using Common Table Expressions (CTEs) via the `WITH` clause, applying `EXISTS/NOT EXISTS`, producing conditional output with `CASE`, creating views, and performing controlled data modification with `UPDATE` and `DELETE`. The lab concludes with business-style reporting queries.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Learning Objectives
- Use subqueries (nested and correlated) to answer complex information needs
- Use the `WITH` clause (CTE) to structure and simplify multi-step queries
- Apply `EXISTS` / `NOT EXISTS` for existence checks
- Create reusable views for derived datasets
- Use set operators (`UNION`, `INTERSECT`, `MINUS`) for list-based querying
- Use `CASE` for conditional classification in query outputs
- Perform safe `UPDATE` and `DELETE` operations based on business rules

## Contents
- `Lab06 - SQL.pdf` — Lab instructions and questions
- `Lab06Demo_SQL.pdf` — Reference/demo examples for covered SQL concepts
- `LAB6_zuha_aqib_26106.sql` — Submitted solution script for Lab 06

## Requirements
- Oracle Database (or Oracle LiveSQL/SQL Developer)
- HR schema available (tables such as `employees`, `departments`, `job_history`, etc.)
- A SQL execution environment:
  - SQL*Plus, SQL Developer, or Oracle LiveSQL

## How to Run
### Option A — SQL*Plus (recommended for local Oracle)
1. Open SQL*Plus and connect to the database:
   ```sql
   sqlplus username/password
   ```

2. Navigate to the lab folder and run the script:

   ```sql
   @LAB6_zuha_aqib_26106.sql
   ```
3. Review results printed to the console.

### Option B — SQL Developer

1. Open SQL Developer and connect to the HR-enabled database.
2. Open `LAB6_zuha_aqib_26106.sql`.
3. Run the script (or run queries section-by-section).

## Task Coverage (High-Level)

The lab script includes queries and operations for:

* Salary comparison using a CTE (`WITH`) and subqueries
* Department-based employee filtering (e.g., IT department)
* Nested subqueries involving manager relationships and location constraints
* Comparisons against averages (global and department-wise)
* `ALL`-based comparisons against a group (e.g., higher than all SA_REP salaries)
* Manager detection using existence checks
* Departments with no employees using `NOT EXISTS`
* Creating a job history view for a specific employee
* Set operator tasks (employees without job history, combined name lists, manager intersections)
* Department salary summaries with `CASE`-based salary categorization
* Controlled updates (commission update, reassignment of managed entities) and deletion
* Business reporting queries (10+ years tenure email list, department-wise KPI-style summary)

## Notes

* Some SQL execution environments (e.g., Oracle LiveSQL) may restrict certain operations or DDL behaviors. If a statement is blocked, the same logic can be executed on a local Oracle instance via SQL*Plus/SQL Developer.
* For reproducibility, it is recommended to run the script against a fresh HR schema state when testing `UPDATE`/`DELETE` sections.

## Academic Integrity

This repository is an academic course archive. The materials are organized for learning and revision, and should be used in accordance with university academic integrity policies.