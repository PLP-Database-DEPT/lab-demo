###  Lab 3: Inserting and Viewing Data in MySQL 

**Lab Duration:** 60–75 minutes


**Learning Objectives**

By the end of this lab, you will be able to:

- Understand what a database and a table are
- Create a database in MySQL
- Create a table with columns and data types
- View and confirm the structure of a table

**Scenario**

You are still working as a Junior Data Assistant at BrightMart Ltd.
The database and employee table are now ready.

Your manager provides a list of employees and asks you to:

Add their details into the database

Confirm the data was saved correctly

Display the data when requested

This is your first time working with real data in MySQL.

**Task 1: Log Into MySQL and Select the Database**

Open Command Prompt or Terminal.
Log in:
```bash
mysql -u root -p
```
Enter your password.

Select the database:
```bash
USE brightmart;
```
**Task 2: Insert One Employee Record**

To add a single employee:
```bash
INSERT INTO employees 
(employee_id, full_name, email, age, department)
VALUES 
(1, 'John Mwangi', 'john.mwangi@brightmart.com', 28, 'Sales');
```
You should see:

_Query OK, 1 row affected_

**Task 3: Insert Multiple Employee Records**
```bash
INSERT INTO employees 
(employee_id, full_name, email, age, department)
VALUES
(2, 'Mary Wanjiku', 'mary.wanjiku@brightmart.com', 32, 'Finance'),
(3, 'Peter Otieno', 'peter.otieno@brightmart.com', 26, 'IT'),
(4, 'Aisha Hassan', 'aisha.hassan@brightmart.com', 29, 'HR');
```

**Task 4: View All Data in the Table**

To see all records:
```bash
SELECT * FROM employees;
```
This displays:
- All columns
- All rows

**Task 5: View Specific Columns**

To view only names and departments:
```bash
SELECT full_name, department FROM employees;
```

**Task 6: View One Record Using a Condition**

To find employees in the IT department:
```bash
SELECT * FROM employees WHERE department = 'IT';
```
