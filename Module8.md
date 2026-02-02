🔹 MODULE 8: Joins (Very Important)

Goal: Combine data from multiple tables using a related column

What is a JOIN?

A JOIN is used to retrieve related data from two or more tables based on a common column.

📌 Usually based on primary key – foreign key relationship

1️⃣ INNER JOIN

Returns only matching rows from both tables.

📌 Most commonly used join.

Definition:

INNER JOIN returns rows where the join condition is satisfied in both tables.

Logic: Intersection of two tables.

2️⃣ LEFT JOIN (LEFT OUTER JOIN)

Returns:

All rows from left table

Matching rows from right table

NULL where no match exists

Definition:

LEFT JOIN keeps all records from the left table, even if no match exists in the right table.

3️⃣ RIGHT JOIN (RIGHT OUTER JOIN)

Returns:

All rows from right table

Matching rows from left table

NULL where no match exists

📌 Less commonly used.

Definition:

RIGHT JOIN keeps all records from the right table.

4️⃣ FULL JOIN (Conceptual)

Returns:

All rows from both tables

Matching where possible

NULL where no match exists

📌 Not supported directly in MySQL
📌 Important conceptually

Definition:

FULL JOIN returns the union of LEFT and RIGHT joins.

5️⃣ SELF JOIN

A table is joined with itself.

📌 Used when data in a table references itself.

Definition:

SELF JOIN is a join where a table is joined to itself using aliases.

🧠 Example (Your Given Query Explained)
SELECT s.name, c.course
FROM students s
JOIN courses c ON s.id = c.student_id;


students → left table

courses → right table

s.id = c.student_id → join condition

JOIN → default is INNER JOIN

📌 Returns only students who are enrolled in a course.