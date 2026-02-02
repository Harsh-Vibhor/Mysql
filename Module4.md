🔹 MODULE 4: Constraints & Data Integrity

Goal: Ensure correct, valid, and consistent data in the database

What are Constraints?

Constraints are rules applied to table columns that restrict the type of data allowed.

📌 They are enforced by the DBMS itself, not the application.

1️⃣ NOT NULL

Ensures that a column cannot have NULL values.

📌 Use when a value is mandatory.

Example:

name VARCHAR(50) NOT NULL

2️⃣ UNIQUE

Ensures all values in a column are different.

📌 Multiple UNIQUE constraints allowed per table.

Example:

email VARCHAR(100) UNIQUE

3️⃣ PRIMARY KEY

Uniquely identifies each row

Combination of:

UNIQUE

NOT NULL

📌 Only one primary key per table
📌 Can be composite

Example:

id INT PRIMARY KEY

4️⃣ FOREIGN KEY

Creates a relationship between tables

Refers to the primary key of another table

📌 Enforces referential integrity

Example:

student_id INT REFERENCES STUDENT(id)


📌 Prevents invalid references.

5️⃣ CHECK

Ensures values satisfy a specific condition.

📌 Used for business rules.

Example:

age INT CHECK (age >= 18)

6️⃣ DEFAULT

Assigns a default value if none is provided.

📌 Prevents NULLs where sensible defaults exist.

Example:

status VARCHAR(20) DEFAULT 'active'

🧠 Important Constraint Rules (Interview-Focused)

A table can have:

Multiple UNIQUE constraints

Only one PRIMARY KEY

PRIMARY KEY ≠ UNIQUE

FOREIGN KEY can be NULL

CHECK enforces domain rules

DEFAULT works only when value is omitted

🎯 Common Interview Traps

PRIMARY KEY automatically creates an index

UNIQUE allows one NULL (DBMS-dependent detail)

FOREIGN KEY ensures referential integrity

Constraints are checked before data is stored