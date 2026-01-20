## Lab 2: Storing Company Data Using MySQL

**Lab Duration:** 60–75 minutes

**Learning Objectives**

By the end of this lab, students will be able to:

- Understand what a database and a table are
- Create a database in MySQL
- Create a table with columns and data types
- View and confirm the structure of a table

**Scenario**

You are continuing your role as a Junior Data Assistant at BrightMart Ltd.
The company wants to start storing employee information digitally instead of using paper files.

Your manager asks you to:
- Create a new database for the company
- Create a table to store employee details

This will be the first real data structure you create in MySQL

**Task 1: Log Into MySQL**

Open Command Prompt or Terminal.

Log in:
```sh
mysql -u root -p
```
Enter your password.
Confirm you see:
```bash
mysql>
```
**Task 2: Create a Database**

At the mysql> prompt, type:
```bash
CREATE DATABASE brightmart;
```
Press Enter.
Confirm creation:
```bash
SHOW DATABASES;
```
You should see brightmart in the list.

**Task 3: Use the Database**

Before creating tables, tell MySQL which database to use.
```bash
USE brightmart;
```
You should see:
_Database changed_

**Task 4: Create Your First Table**

You will create a table called employees.
```bash
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100),
    age INT,
    department VARCHAR(50)
);
```
Press Enter.
If successful, MySQL will respond:
_Query OK_

**Task 5: View Tables in the Database**
```bash
SHOW TABLES;
```
You should see: _employees_

**Task 6: View Table Structure**

To see the columns and data types:
```bash
DESCRIBE employees;
```
This shows:
- Column names
- Data types
- Primary key

**Validation Checklist**

- [x] Database created successfully
- [x] Table created without errors
- [x] Table structure can be viewed
- [x] Student understands rows vs columns
