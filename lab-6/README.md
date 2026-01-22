## Lab 6: Organizing and Controlling Query Results


## Lab Duration

60 minutes

## Learning Objectives

By the end of this lab, students will be able to:

* Sort results using ORDER BY
* Limit results using LIMIT
* Combine ORDER BY and LIMIT
* Produce clean, readable outputs

---

## Scenario

Your manager wants reports that:

* Show employees ordered by age
* Display only the top few results
* Avoid overwhelming output

You must **organize and control** the results.

---

## Task 1: Sort Data Using ORDER BY (Ascending)

```
SELECT * FROM employees
ORDER BY age;
```

(Default is ascending)

---

## Task 2: Sort Data Using ORDER BY (Descending)

```
SELECT * FROM employees
ORDER BY age DESC;
```

---

## Task 3: Limit the Number of Results

Show only the first 2 employees:

```
SELECT * FROM employees
LIMIT 2;
```

---

## Task 4: Combine ORDER BY and LIMIT

Show the two oldest employees:

```
SELECT * FROM employees
ORDER BY age DESC
LIMIT 2;
```

---

## Why This Matters

* Sorting improves readability
* LIMIT improves performance
* Reports become more useful

---

## Validation Checklist

* ORDER BY sorts correctly
* DESC reverses order
* LIMIT restricts rows returned

---

## Reflection Questions

1. What is the default order in ORDER BY?
2. Why is LIMIT useful in large databases?
3. How does ORDER BY help decision-making?

---

## Lab Outcome

You can now:

* Sort data
* Control result size
* Produce professional query outputs

---

**End of Lab 6**
