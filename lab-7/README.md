## Hands-on SQL Lab

#### Project Duration

60 min

### Prerequisites

You must have completed:

* Lab 1: Installation
* Lab 2: CREATE DATABASE, CREATE TABLE
* Lab 3: INSERT, SELECT
* Lab 4: UPDATE, DELETE
* Lab 5: WHERE, AND, OR
* Lab 6: ORDER BY, LIMIT
* Lab 7: Normalization (1NF, 2NF, 3NF)

---

### Project Scenario

You have been hired by **BrightFuture Training Institute**.

The institute currently stores student data in notebooks and Excel sheets.
They want a **simple MySQL database system** to:

* Store student details
* Store courses offered
* Record student enrollments
* Retrieve meaningful reports

Your task is to **design, normalize, and implement** the database using MySQL.

---

### Project Objectives

By completing this project, students will:

* Design a small real-world database
* Apply normalization principles
* Create multiple related tables
* Insert realistic data
* Write basic queries to retrieve and manage data

---

### Business Rules

1. One student can enroll in many courses
2. One course can have many students
3. Each enrollment records the date of enrollment
4. No duplicate data should exist

---

## Part 1: Database Design (Planning)

### Entities Identified:

* Students
* Courses
* Enrollments

### Normalization Applied:

* Student details stored once
* Course details stored once
* Enrollments stored separately

---

## Part 2: Create the Database

```
CREATE DATABASE student_management;
USE student_management;
```

---

## Part 3: Create Tables

### 1. Students Table

```
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100),
    phone VARCHAR(20)
);
```

---

### 2. Courses Table

```
CREATE TABLE courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100),
    duration_weeks INT
);
```

---

### 3. Enrollments Table

```
CREATE TABLE enrollments (
    enrollment_id INT PRIMARY KEY,
    student_id INT,
    course_id INT,
    enrollment_date DATE
);
```

*(Foreign keys will be introduced in a later lab.)*

---

## Part 4: Insert Sample Data

### Students

```
INSERT INTO students VALUES
(1, 'John Mwangi', 'john@gmail.com', '0712345678'),
(2, 'Mary Wanjiku', 'mary@gmail.com', '0723456789'),
(3, 'Peter Otieno', 'peter@gmail.com', '0734567890');
```

---

### Courses

```
INSERT INTO courses VALUES
(101, 'Introduction to MySQL', 6),
(102, 'Web Development Basics', 8),
(103, 'Python Programming', 10);
```

---

### Enrollments

```
INSERT INTO enrollments VALUES
(1, 1, 101, '2025-01-10'),
(2, 1, 103, '2025-01-12'),
(3, 2, 101, '2025-01-11'),
(4, 3, 102, '2025-01-15');
```

---

## Part 5: Data Retrieval Tasks (SELECT)

### Task 1

Display all students.

```
SELECT * FROM students;
```

---

### Task 2

Display all courses ordered by duration.

```
SELECT * FROM courses
ORDER BY duration_weeks ASC;
```

---

### Task 3

Show the first 2 enrollments.

```
SELECT * FROM enrollments
LIMIT 2;
```

---

## Part 6: Filtering Data (WHERE, AND, OR)

### Task 4

Find students with phone numbers starting with `07`.

```
SELECT * FROM students
WHERE phone LIKE '07%';
```

---

### Task 5

Find courses longer than 6 weeks.

```
SELECT * FROM courses
WHERE duration_weeks > 6;
```

---

## Part 7: Updating and Deleting Data

### Task 6

Update a student phone number.

```
UPDATE students
SET phone = '0799999999'
WHERE student_id = 2;
```

---

### Task 7

Delete a course that is no longer offered.

```
DELETE FROM courses
WHERE course_id = 103;
```

---

**End**
