# Lab 5: Filtering Data Using WHERE, AND, OR

## Lab Title

**Lab 5: Finding Specific Employees in the Database**


## Lab Duration

60 minutes

## Learning Objectives

By the end of this lab, students will be able to:

* Filter data using WHERE
* Combine conditions using AND and OR
* Retrieve only the data they need

---

## Scenario

Your manager frequently asks questions such as:

* Who works in Finance?
* Which employees are older than 30?
* Who works in Finance and is above 30 years old?

You must use **filters** to answer these questions.

---

## Task 1: View All Employees

```
SELECT * FROM employees;
```

---

## Task 2: Filter Using WHERE

Find employees in the Finance department:

```
SELECT * FROM employees
WHERE department = 'Finance';
```

---

## Task 3: Use WHERE with Numbers

Find employees older than 30:

```
SELECT * FROM employees
WHERE age > 30;
```

---

## Task 4: Use AND

Find employees in Finance **and** older than 30:

```
SELECT * FROM employees
WHERE department = 'Finance'
AND age > 30;
```

---

## Task 5: Use OR

Find employees in Sales **or** IT:

```
SELECT * FROM employees
WHERE department = 'Sales'
OR department = 'IT';
```

---

## Key Rule

* **AND** → all conditions must be true
* **OR** → at least one condition must be true

---

## Validation Checklist

* WHERE filters data correctly
* AND combines conditions correctly
* OR expands search results

---

## Reflection Questions

1. What is the difference between AND and OR?
2. When would you use OR instead of AND?
3. Why is filtering important in databases?

---

## Submission Requirements

* Screenshots of:

  * One WHERE query
  * One AND query
  * One OR query

File name format:
**Lab5_MySQL_Where_And_Or_StudentName**

---

## Lab Outcome

You can now:

* Search data intelligently
* Answer business questions using filters

**Next Lab:**
Sorting and Limiting Results

---

**End of Lab 5**
