# Lab 02 — SQL Aggregations + SQL Functions (HR Schema)

This lab builds directly on the HR schema from Lab 01 and is split into two parts:
- **Lab 02A (Aggregations):** GROUP BY / HAVING + aggregate functions
- **Lab 02B (Functions):** string, numeric, and date functions for transforming query output

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Prerequisites
- HR schema is available (same schema/user from Lab 01)
- Oracle SQL Developer (or Oracle LiveSQL as a backup)

---

## Learning Objectives

### Part A — SQL Aggregations (Lab 02A)
- Use `GROUP BY` and `ORDER BY`
- Filter grouped results using `HAVING`
- Apply aggregate functions: `SUM`, `AVG`, `MIN`, `MAX`, `COUNT`, `DISTINCT`
- Handle NULL values correctly in aggregations
- Produce department/job/location-level summaries (counts, totals, averages)

Example task types include:
- counting employees by department / by condition
- computing average/min/max salary for specific job groups
- department-wise/job-wise salary totals (with thresholds)
- job duration calculations using date differences
- country-wise location counts

---

### Part B — SQL Functions (Lab 02B)
Practice single-row functions (one output row per input row) including:

**Character functions**
- Case conversion: `UPPER`, `LOWER`, `INITCAP`
- Manipulation: `CONCAT`, `SUBSTR`, `LENGTH`, `INSTR`, `LPAD`, `RPAD`, `REPLACE`, `TRIM`, `LTRIM`, `RTRIM`

**Numeric functions**
- `ROUND`, `TRUNC`, `MOD`

**Date functions & date formatting**
- `SYSDATE`, arithmetic on dates
- `MONTHS_BETWEEN`, `ADD_MONTHS`, `NEXT_DAY`, `LAST_DAY`
- `ROUND`, `TRUNC` on dates
- `TO_CHAR` for extracting month/year formats and solving “hired in month X” type questions

---

## Folder Contents
- `Lab02A - SQL Aggregation.pdf` — lab tasks + submission requirements for aggregations
- `Lab02B - SQL Functions.pdf` — lab tasks + submission requirements for functions
- `Lab02Demo_Functions and Aggregations.pdf` — demo/lecture slides for Lab 02 topics
- `LAB2A_zuhaaqib_26106.sql` — solved queries for Lab 02A (question-wise with comments)
- `LAB2B_zuhaaqib_26106.sql` — solved queries for Lab 02B (question-wise with comments)

---

## How to Run (SQL Developer)
1. Open **Oracle SQL Developer**
2. Connect to your Lab 01 HR schema user
3. Open and run:
   - `LAB2A_zuhaaqib_26106.sql`
   - `LAB2B_zuhaaqib_26106.sql`

Tip: Run query-by-query if you want to verify outputs gradually.

---

## Notes
- Aggregations: remember `WHERE` filters rows *before* grouping, while `HAVING` filters groups *after* `GROUP BY`.
- Functions: use them to standardize formatting (case, spacing), extract substrings, and compute time-based measures (experience, durations).
- Avoid committing real credentials/screenshots of passwords to public repos (use placeholders if needed).
