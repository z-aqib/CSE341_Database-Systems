# Lab 12 — MongoDB Setup + Intro to MongoDB (NoSQL)

## Overview
Lab 12 introduces MongoDB and basic NoSQL concepts through a two-part workflow:
1) MongoDB environment setup (local or cloud-based)
2) Hands-on CRUD querying using JSON datasets in MongoDB collections

The lab focuses on understanding document-based storage, MongoDB query syntax, and how common database tasks (filtering, updating, deleting, sorting) are performed in a NoSQL environment.

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Learning Objectives
- Set up MongoDB (local installation or cloud cluster)
- Connect to MongoDB using appropriate tooling
- Import JSON data into collections
- Perform CRUD operations in MongoDB:
  - `find()` queries with filters
  - projections (selecting fields)
  - sorting and limiting results
  - updates (`updateOne`, `updateMany`)
  - deletions (`deleteOne`, `deleteMany`)
- Query nested fields and arrays within documents
- Compare document-based modeling concepts with relational SQL approaches

---

## Contents
### Lab Documents
- `Lab12A - MongoDB Setup Guide.pdf` — setup instructions
- `Lab12B - Intro to MongoDB.pdf` — MongoDB queries + tasks

### Data / Practice Files
- `restaurants.json` — dataset for import and querying
- `practice_lec12A.sql` — optional practice/reference file (if included by course material)

### Submission
- `Lab12_zuha_aqib_26106.docx` — submission/report (screenshots + answers)

---

## Environment Setup (High-Level)
MongoDB can be used in either mode depending on lab requirements:
- **Local MongoDB** (MongoDB Community Server)
- **Cloud MongoDB** (MongoDB Atlas)

After setup:
- Create a database and collection
- Import the provided JSON dataset into the collection

---

## Importing Dataset (Example Workflow)
A typical import flow for JSON datasets is:
1. Create/select a database
2. Create/select a collection
3. Import `restaurants.json` into the collection using a MongoDB import tool or UI
4. Verify document count and sample documents using `find()` and `countDocuments()`

(Exact steps depend on whether local MongoDB or Atlas is used.)

---

## Query Practice (What this lab covers)
This lab includes MongoDB queries for:
- Filtering documents with conditions (e.g., by cuisine, borough, rating thresholds)
- Projection to return only required fields
- Sorting results (ascending/descending)
- Limiting output for pagination-style querying
- Updates to modify fields in documents (single/multiple updates)
- Deletes to remove documents safely based on conditions
- Querying nested objects and arrays (document-style data)