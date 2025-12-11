# Lab 10 — Transactions and Concurrency (Oracle)

## Overview
This lab introduces fundamental concepts of **transaction management** and **concurrency control** in Oracle Database. The exercises are performed using **multiple SQL\*Plus sessions** to simulate concurrent users operating on the same schema.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Objectives
- Understand transaction boundaries and the effect of **autocommit**.
- Observe **visibility rules** for uncommitted vs committed data across sessions.
- Practice `COMMIT`, `ROLLBACK`, and `SAVEPOINT` for safe recovery.
- Recognize why multi-step updates should be committed **as a single unit** (atomicity).
- Simulate and analyze a **deadlock** (ORA-00060).
- Prevent deadlocks using `SELECT ... FOR UPDATE` row locking.
- Demonstrate the **lost update** anomaly.
- Apply and observe Oracle’s **READ COMMITTED** isolation behavior during concurrent updates.

## Prerequisites
- Oracle Database installed locally (required for multi-session SQL\*Plus execution).
- SQL\*Plus access (two terminal windows recommended).
- Oracle SQL Developer may be used for convenience, but concurrency must be tested via parallel sessions.

## Contents
- `Lab10 - Transactions and Concurrency.pdf`  
  Official lab handout and follow-along instructions.
- `zuha_aqib_26106_lab10.docx`  
  Submission report with required screenshots and short explanations (as per lab instructions).
- *(Optional)* Any supporting `.sql` scripts created during the lab (if included in this folder).

## Setup (Sessions)
1. Open **SQL\*Plus Session 01** and log in as `sysdba`.
2. Create a dedicated user for the lab and grant required privileges.
3. Open **SQL\*Plus Session 02** in a second terminal and connect using the same lab user.
4. Disable autocommit where required:
   ```sql
   SET AUTOCOMMIT OFF;
    ```

## Exercises Summary

### 1) Table Setup

* Create sample tables (e.g., `toys`, `bricks`) and insert initial records.

### 2) Commit Visibility Across Sessions

* Insert rows in Session 01 without committing.
* Verify whether Session 02 can see the changes.
* Commit in Session 01 and verify visibility again.

### 3) Rollback and Savepoints

* Use `ROLLBACK` to undo changes since the last commit.
* Use `SAVEPOINT` and `ROLLBACK TO SAVEPOINT` to undo only part of the work.

### 4) Multi-step Updates as One Transaction

* Perform two related updates (e.g., decrement one set of rows and increment another).
* Commit once at the end to preserve atomicity and avoid partial updates.

### 5) Deadlock Simulation (ORA-00060)

* Execute conflicting updates in both sessions in different orders to create a circular wait.
* Observe Oracle detecting the deadlock and aborting one statement.

### 6) Preventing Deadlocks with `SELECT ... FOR UPDATE`

* Lock required rows first using:

  ```sql
  SELECT * FROM bricks
  WHERE colour IN ('red', 'blue')
  FOR UPDATE;
  ```
* Perform updates safely after acquiring locks.

### 7) Lost Update Demonstration

* Simulate two users updating the same row where each overwrites the other’s changes by updating unchanged columns with stale values.

### 8) Isolation Level: READ COMMITTED

* Set transaction isolation level and observe blocking behavior when another session holds uncommitted changes:

  ```sql
  SET TRANSACTION ISOLATION LEVEL READ COMMITTED;
  ```

## Notes

* Screenshots and short explanations are required for submission documentation (included in the `.docx` file).
* Any credentials shown in screenshots should be treated as sensitive; avoid publishing real passwords in public repositories.