🔹 MODULE 5: Keys & Relationships

Goal: Link tables correctly and safely

1️⃣ Primary Key

Uniquely identifies each record in a table

Cannot be NULL

Only one per table

📌 Ensures entity integrity

Example:

STUDENT(id PRIMARY KEY)

2️⃣ Foreign Key

A column that refers to a primary key in another table

Creates a relationship between tables

📌 Can be NULL
📌 Ensures referential integrity

Example:

ENROLLMENT(student_id → STUDENT.id)

3️⃣ Composite Key

A primary key made of more than one column

Used when a single column is not enough

📌 Common in junction tables

Example:

PRIMARY KEY (student_id, course_id)

4️⃣ Surrogate Key

Artificial, system-generated key

Has no business meaning

📌 Often auto-incremented

Example:

id INT AUTO_INCREMENT


📌 Used for simplicity and performance

5️⃣ Referential Integrity

Ensures that:

A foreign key value must exist in the referenced table

Or be NULL

📌 Prevents orphan records

Example:
You cannot enroll a student who doesn’t exist.

6️⃣ Types of Relationships
🔹 One-to-One (1:1)

One record in table A relates to one record in table B

📌 Rare in practice
📌 Often used to split sensitive data

🔹 One-to-Many (1:N)

One record in table A relates to many records in table B

📌 Most common relationship

Example:

One student → many enrollments

🔹 Many-to-Many (M:N)

Many records in table A relate to many in table B

Implemented using a junction table

📌 Requires composite primary key + foreign keys

Example:
STUDENT ↔ COURSE via ENROLLMENT