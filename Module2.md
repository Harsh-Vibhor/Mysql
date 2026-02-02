🔹 MODULE 2: Relational Model & Terminology

Goal: Understand how data is structured in a relational database

1️⃣ Table (Relation)

A table is a collection of related data organized in rows and columns.

📌 In relational DBMS, a table is formally called a relation.

Example:
STUDENT

2️⃣ Row (Tuple)

A row represents one complete record in a table.

📌 In DBMS terms, a row is called a tuple.

Example:

(101, Harsh, 21)

3️⃣ Column (Attribute)

A column represents a property of the data.

📌 In DBMS terms, a column is called an attribute.

Example:

id, name, age

4️⃣ Schema vs Instance
Schema

Logical structure of the database

Defined once

Rarely changes

Example:

STUDENT(id, name, age)

Instance

Actual data stored at a particular time

Changes frequently

Example:

(101, Harsh, 21)
(102, Ankit, 22)


📌 One-liner:

Schema is the blueprint, instance is the current data.

5️⃣ Degree & Cardinality
Degree

Number of columns in a table

Example:
STUDENT(id, name, age) → Degree = 3

Cardinality

Number of rows in a table

Example:
5 student records → Cardinality = 5

6️⃣ Super Key

A super key is any set of attributes that can uniquely identify a row.

Examples:

{id}

{id, name}

{id, age}

📌 May contain extra attributes.

7️⃣ Candidate Key

A candidate key is a minimal super key.

📌 No extra attributes.

Example:

{id} (if id uniquely identifies students)

8️⃣ Primary Key

A primary key is the chosen candidate key used to identify records.

📌 Rules:

Unique

Not NULL

Only one per table

Example:

id → Primary Key

9️⃣ Foreign Key

A foreign key is an attribute in one table that refers to the primary key of another table.

📌 Used to create relationships.

Example:

ENROLLMENT(student_id) → STUDENT(id)

🧠 Example Table Understanding
STUDENT(id, name, age)


Table name → STUDENT

Attributes → id, name, age

Degree → 3

Tuple example → (101, Harsh, 21)

Primary key → id