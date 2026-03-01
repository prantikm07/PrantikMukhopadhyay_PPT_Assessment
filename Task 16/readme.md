# Task 16: RDS Database + SQL Workbench Connection & Queries

## Simple Definition

Amazon RDS is a managed relational database service that simplifies database setup, operation, and scaling.

## Objective

To create an RDS database, connect using SQL Workbench, and execute basic SQL queries.

## Architecture Overview

Client (SQL Workbench)  
↓  
Amazon RDS Instance  
↓  
Managed Database Engine (MySQL/PostgreSQL)

## Steps

### Step 1: Create RDS Instance

1. Go to RDS → Create Database.
2. Select Standard Create.
3. Choose engine (MySQL).
4. Set DB instance identifier.
5. Set master username and password.
6. Choose instance class.
7. Enable Public access (for testing).
8. Create database.

### Step 2: Configure Security Group

1. Allow inbound MySQL (Port 3306).
2. Add your IP address.

### Step 3: Connect via SQL Workbench

1. Open SQL Workbench.
2. Enter:
   - Hostname: RDS endpoint.
   - Port: 3306.
   - Username and password.
3. Connect.

### Step 4: Execute Queries

Run sample queries:

CREATE DATABASE testdb;
USE testdb;
CREATE TABLE students (id INT, name VARCHAR(50));
INSERT INTO students VALUES (1, 'John');
SELECT * FROM students;

## Verification

* RDS status = Available.
* Successful SQL connection.
* Query output visible.
* Data inserted and retrieved.

## Conclusion

Successfully created and connected to Amazon RDS database and executed SQL queries, demonstrating managed database service usage.