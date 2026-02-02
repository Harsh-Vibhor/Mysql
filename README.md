# Mysql
A personal learning repository for practicing and documenting programming concepts in Mysql.

📘 DBMS Mini Syllabus (Structured Roadmap)

🔹 MODULE 1: Database Basics (Foundations)

Goal: Understand why databases exist

What is Data vs Information

What is DBMS

Advantages of DBMS

Types of Databases

✅ Outcome: You know what a DBMS solves

🔹 MODULE 2: Relational Model & Terminology

Goal: Learn how data is structured

Table (Relation)

Row (Tuple)

Column (Attribute)

Schema vs Instance

Degree & Cardinality

Primary Key

Candidate Key

Super Key

Foreign Key

Example table understanding:

STUDENT(id, name, age)

🔹 MODULE 3: SQL Language Categories (Very Important)

Goal: Understand types of SQL commands

🟦 1. DDL – Data Definition Language

Used to define structure

CREATE

ALTER

DROP

TRUNCATE

Example:

CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(50)
);

🟩 2. DML – Data Manipulation Language

Used to modify data

INSERT

UPDATE

DELETE

Example:

INSERT INTO users VALUES (1, 'Harsh');

🟨 3. DQL – Data Query Language

Used to fetch data

SELECT

Example:

SELECT * FROM users;

🟥 4. DCL – Data Control Language

Used for permissions

GRANT

REVOKE

🟪 5. TCL – Transaction Control Language

Used for transactions

COMMIT

ROLLBACK

SAVEPOINT

✅ Outcome: You know what each SQL command type does

🔹 MODULE 4: Constraints & Data Integrity

Goal: Keep data correct

NOT NULL

UNIQUE

PRIMARY KEY

FOREIGN KEY

CHECK

DEFAULT

Example:

age INT CHECK (age >= 18)

🔹 MODULE 5: Keys & Relationships

Goal: Link tables properly

Primary Key

Foreign Key

Composite Key

Surrogate Key

Referential Integrity

Relationships:

One-to-One

One-to-Many

Many-to-Many

🔹 MODULE 6: Normalization

Goal: Reduce redundancy

Functional Dependency

1NF (First Normal Form)

2NF

3NF

BCNF (basic idea)

Why normalization matters
Examples of bad vs good design

🔹 MODULE 7: SQL Queries (Core Skills)

Goal: Actually query data

WHERE

ORDER BY

GROUP BY

HAVING

LIMIT

Aggregate Functions:

COUNT

SUM

AVG

MIN, MAX

🔹 MODULE 8: Joins (Very Important)

Goal: Work with multiple tables

INNER JOIN

LEFT JOIN

RIGHT JOIN

FULL JOIN (conceptual)

SELF JOIN

Example:

SELECT s.name, c.course
FROM students s
JOIN courses c ON s.id = c.student_id;

🔹 MODULE 9: Subqueries & Views

Goal: Advanced querying

Subqueries (nested queries)

Correlated subqueries

IN, EXISTS

Views

CREATE VIEW active_users AS
SELECT * FROM users WHERE status = 'active';

🔹 MODULE 10: Indexing & Performance (Must-Know)

🔹 MODULE 11: Transactions, ACID & Concurrency (Must-Know)

🔹 MODULE 12: DBMS Architecture, Security & NoSQL (Awareness Level)
