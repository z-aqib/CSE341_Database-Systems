# Lab 04 — ERD Design (Chen + Crow’s Foot + DB Designer)

This lab is about converting real-world requirements into correct ERDs and then producing an
implementation-ready relational design using DB Designer. You practice:
- Chen’s notation (conceptual)
- Crow’s Foot notation (logical)
- DB Designer ERD (implementation) + SQL export

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

---

## Objectives
- Identify entities, attributes, and relationships from a problem statement
- Decide correct cardinalities (1–1, 1–M, M–N) and resolve M–N using associative entities
- Choose primary keys and implement foreign keys correctly
- Convert ERD → relational schema and export the DDL SQL from DB Designer

---

## Submission (what the lab expects)
- Work is compiled in a Word document (template provided)
- Diagrams for all scenarios are included (images/screenshots)
- DB Designer export can be used to generate SQL scripts

---

## Scenarios Covered

### Scenario 1 — University Enrollment System
Design a registrar system that stores:
- Courses (code, title, credits, syllabus)
- Course offerings (class number, semester/year, timings, classroom, instructor)
- Students (ERP, name, email, DOB, program)
- Instructors (ERP, name, department, job title)
- Enrollment (student ↔ offering + grade)
- Prerequisites (course ↔ prerequisite course mapping)

Deliverables:
- Conceptual ERD (Chen)
- DB Designer implementation ERD
- Exported SQL

---

### Scenario 2 — Cricket Tournament System
Design a tournament DB with:
- Countries/Teams and Players (each player belongs to a country/team)
- Stadiums (city, capacity)
- Umpires (belonging to countries)
- Matches (two teams, two selected umpires, stadium, date/time, winner, man of the match)
- Player performance per match (runs, wickets)

Deliverables:
- Crow’s Foot ERD
- DB Designer implementation ERD
- Exported SQL

---

### Scenario 3 — Hotel Management System
Design a hotel DB with:
- Floors and Rooms (multi-floor building)
- Dining Halls (located on floors)
- Room categories and occupancy types
- Room pricing (defined by category + occupancy type)
- Facilities per category
- Dining hall assignment for breakfast/lunch/dinner per room

Deliverables:
- ERD (logical + implementation)
- Exported SQL

---

## Folder Contents
Lab handouts / references:
- `Lab04_ERD Design.pdf` — lab instructions
- `Lab04_Template_forSubmission.docx` — submission template
- `Lab04-Solution.pdf` — suggested solutions (for reference)

- `lab04_q1_1.png` — Scenario 1 ERD image (Enrollment)
- `lab04_q2_1.png` — Scenario 2 ERD image (Cricket)
- `lab04_q3.jpg` — Scenario 3 ERD image (Hotel)

DB Designer exports:
- `lab04_q1-*.sql` — exported DDL for Scenario 1
- `lab04_q2-*.sql` — exported DDL for Scenario 2

---

## How to Export SQL from DB Designer (recommended workflow)
1. Create tables/entities and define attributes + PKs
2. Add relationships and set cardinalities
3. Ensure FK fields exist on the correct side (many-side holds the FK)
4. Use **Export → SQL** and select **Oracle**
5. Save the `.sql` export into this lab folder

---

## Notes / Tips
- If you get a many-to-many relationship, resolve it with a bridge table (associative entity).
- Keep naming consistent (singular table names, snake_case or consistent casing).
- Prefer surrogate PKs where needed, but natural keys are fine if truly stable (e.g., course_code).
