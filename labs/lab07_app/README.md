# Lab 07 — App Development with Oracle Database (Employee Management System)

## Overview
Lab 07 serves as an introductory guide to web application development for Database Systems and demonstrates how an Oracle Database is connected to a web application to perform CRUD (Create, Read, Update, Delete) operations. A compact OLTP Employee-Management System is provided using the Oracle HR schema. 

Course: **CS 341 — Database Systems (Fall 2024)**    
University: **Institute of Business Administration (IBA), Karachi, Pakistan**    
Instructor: **Abeera Tariq**    

## Key Topics
- Oracle DB connectivity from a Node.js/Express backend
- REST APIs for CRUD operations (GET, POST, PUT, DELETE)
- MVC architecture (Models, Controllers, Routes, Config, App initialization)
- API testing using Postman collections
- Environment-based secrets management using `.env` (not committed to GitHub)

## Prerequisites
- Node.js (v20 LTS)
- Git
- Postman
- Oracle Database installed with a user that has the HR schema loaded

## Project Structure
This lab includes a complete full-stack application with separate backend and frontend folders.{index=8}

High-level layout (see repository tree for full detail):
- `lab7-dbms-app/backend/`
  - `config/db.js` (Oracle connection configuration)
  - `models/` (database query layer)
  - `controllers/` (request handlers and business logic)
  - `routes/` (REST endpoints mapped to controllers)
  - `middlewares/` (authentication/guards)
  - `postman/` (Postman collection)
  - `app.js` (Express app initialization)
- `lab7-dbms-app/frontend/`
  - UI for interacting with the backend APIs 

## Setup Instructions

### 1) Backend Setup
1. Open a terminal in:
   ```bash
   labs/lab07_app/lab7-dbms-app/backend
    ```

2. Create a local `.env` file by copying/renaming the sample:

   * Rename `.env.sample` → `.env`
   * Update Oracle credentials and connection string in `.env` 
3. Install dependencies and start the backend:

   ```bash
   npm install
   npm run start
   ```
4. Confirm the backend is running by opening:

   * `http://localhost:3001/`
   * Example API (employees listing): `http://localhost:3001/api/employees` 

### 2) Frontend Setup

1. Open a terminal in:

   ```bash
   labs/lab07_app/lab7-dbms-app/frontend
   ```
2. Install dependencies and start the frontend:

   ```bash
   npm install
   npm start
   ```

## API Testing (Postman)

The backend folder contains a Postman collection that can be imported to test endpoints without using the UI. After importing, the collection provides API calls such as listing employees and other CRUD operations. 

## Architecture Notes (MVC)

The application follows the MVC pattern:

* **Routes** map URLs + HTTP methods to controller functions.
* **Controllers** process requests and call model functions.
* **Models** interact with Oracle DB and execute SQL queries.
* **Config** contains DB connection setup (`db.js`).
* `app.js` initializes Express, middleware, and routes. 

## Lab-Specific Implementation Note (Departments Listing)

As part of Lab 07 work, the application was extended by adding support for listing departments similar to employee listing:

* Added a controller function for retrieving departments.
* Connected it through department routes.
* Implemented the corresponding model function for database retrieval.
* Verified the endpoint via Postman and resolved a route path mismatch, requiring a restart of backend/frontend to load changes correctly. 

## Security Note

Do not commit `.env` files or database credentials to GitHub. The lab provides `.env.sample` to support safe local configuration. 