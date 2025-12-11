# Lab 05 — SQL Joins (Oracle HR Schema)

This folder contains materials and solutions for **Lab 05: Joins** in **CSE341 — Database Systems**.  
The lab is based on the **Oracle HR schema** and emphasizes constructing correct multi-table queries using join operations.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Learning Outcomes

Lab 05 develops proficiency in:

- Understanding common join types: **INNER**, **LEFT OUTER**, **RIGHT OUTER**, and **FULL OUTER** joins.
- Writing joins using multiple equivalent syntaxes:
  - Cartesian product with `WHERE`
  - `JOIN ... USING`
  - `JOIN ... ON`
  - `NATURAL JOIN`
- Applying joins to real-world reporting queries across HR tables (employees, departments, locations, jobs).
- Using **self-joins** for hierarchical relationships (employee ↔ manager).
- Using **outer joins** to include unmatched rows (e.g., departments without employees).

---

## Included Files

- `Lab05_Joins.pdf` — official lab questions and requirements.
- `Lab05Demo_Joins.pdf` — demo/lecture slides covering join concepts and syntax.
- `lab05_zuha_aqib_26106.sql` — SQL solution script (question-wise queries).

---

## Requirements

- Oracle Database with the **HR schema** available (same dataset used in earlier SQL labs).
- Oracle SQL Developer (recommended) or SQL*Plus.

---

## How to Run

1. Open **Oracle SQL Developer**.
2. Connect to the schema where the HR tables are available.
3. Open `lab05_zuha_aqib_26106.sql`.
4. Execute queries section-by-section to verify outputs.

---

## Topics Covered (High-Level)

This lab includes join-based queries for:

- Employee + Department output using multiple join syntaxes.
- Employee + Department + Location reporting (city/state/country context).
- Employee + Job Title mappings.
- Filters across joined data (department names, city prefixes, department suffix patterns).
- Manager relationships using self-joins (including employees without managers).
- Outer join reporting:
  - Employees with no department
  - Departments with no employees
  - Full outer join coverage
- Advanced join logic:
  - Employees earning more than their managers
  - Date-window filtering across related tables
  - Aggregations on joined datasets (e.g., average salary per department, counts per job title)

---

## Notes

- Prefer `JOIN ... ON` when join columns have different names or when complex join conditions are needed.
- Use consistent table aliases to improve readability in multi-table queries.
- Avoid committing any real credentials (password screenshots/text) to public repositories.
