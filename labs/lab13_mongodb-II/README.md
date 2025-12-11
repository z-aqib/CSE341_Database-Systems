# Lab 13 — MongoDB II (Advanced MongoDB Queries + Aggregation)

## Overview
Lab 13 extends MongoDB fundamentals by focusing on advanced querying techniques and aggregation pipelines. The lab practices importing structured data into MongoDB, writing compound queries, and generating summarized outputs using MongoDB’s aggregation framework.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Learning Objectives
- Import datasets into MongoDB collections (including CSV-based data)
- Write advanced `find()` queries using compound filters and logical operators
- Apply projections, sorting, and limiting for controlled result output
- Use aggregation pipelines for analytics-style results:
  - `$match` for filtering
  - `$group` for summarization
  - `$sort` for ordered outputs
  - `$project` for reshaping results
- Produce reporting-friendly outputs from semi-structured document data

---

## Contents
- `Lab13 - MongoDB II.pdf` — official lab instructions and tasks
- `lab_13_zuha_aqib_26106.docx` — submission/report (screenshots + answers)
- `orders.csv` — dataset used for import and query practice

---

## Requirements
- MongoDB (local installation or MongoDB Atlas)
- MongoDB shell / Compass / Atlas UI (any tool suitable for importing and querying)
- A database and collection created for Lab 13 datasets

---

## Dataset Import (High-Level)
1. Create/select a MongoDB database for Lab 13.
2. Create/select a collection (e.g., `orders`).
3. Import `orders.csv` into the collection using:
   - MongoDB Compass import feature, or
   - an appropriate CLI import tool
4. Verify import success by checking document count and viewing sample documents.

---

## Query Practice (What this lab covers)
This lab includes tasks involving:
- Compound filters on multiple fields
- Sorting and limiting results for top-k style outputs
- Field projection to return only relevant attributes
- Aggregation pipelines for computed summaries (counts, totals, grouped analytics)
- Output shaping for readable reporting