## Lab 4: Correcting and Removing Employee Records


## Lab Duration

60 minutes

## Learning Objectives

By the end of this lab, students will be able to:

* Update existing records using UPDATE
* Delete records using DELETE
* Understand why WHERE is critical when modifying data
* Avoid common beginner mistakes that cause data loss

---

## Scenario

After entering employee data, your manager at **BrightMart Ltd** notices some mistakes:

* One employee’s department is incorrect
* One employee has left the company and must be removed from the system

You are asked to **correct the data safely** without affecting other records.

---

## Task 1: Log In and Select the Database

```
mysql -u root -p
USE brightmart;
```

---

## Task 2: View Current Employee Data

Before making changes, always check the data:

```
SELECT * FROM employees;
```

---

## Task 3: Update an Employee Record

Peter Otieno has moved from IT to Finance.

```
UPDATE employees
SET department = 'Finance'
WHERE employee_id = 3;
```

Verify the change:

```
SELECT * FROM employees WHERE employee_id = 3;
```

---

## Task 4: Update Multiple Columns

Mary Wanjiku’s age was entered incorrectly. She is 33.

```
UPDATE employees
SET age = 33
WHERE employee_id = 2;
```

---

## Task 5: Delete an Employee Record

Aisha Hassan has left the company.

```
DELETE FROM employees
WHERE employee_id = 4;
```

Verify deletion:

```
SELECT * FROM employees;
```

---

## Very Important Warning

**Never run UPDATE or DELETE without a WHERE clause.**
Doing so will change or delete **all records**.

---

## Validation Checklist

* UPDATE changes only the intended record
* DELETE removes only one record
* Data remains consistent after changes

---

## Reflection Questions

1. Why is WHERE important in UPDATE and DELETE?
2. What could happen if you forget the WHERE clause?
3. When should data be updated instead of deleted?

---

## Lab Outcome

You can now safely:

* Modify existing data
* Remove unwanted records

**Next Lab:**
Filtering Data Using WHERE, AND, OR

---

**End of Lab 4**
