🔹 MODULE 6: Normalization

Goal: Reduce redundancy, avoid anomalies, and design clean tables

Why Normalization Matters (Start Here)

Without normalization, databases suffer from:

Data redundancy (same data repeated)

Update anomaly (change in one place, forgotten in another)

Insertion anomaly (can’t insert data without unrelated data)

Deletion anomaly (deleting data causes unintended loss)

📌 One-line purpose:

Normalization organizes data to reduce redundancy and maintain consistency.

1️⃣ Functional Dependency (FD)

A functional dependency exists when:

One attribute uniquely determines another.

Notation:

A → B


Meaning:
If A is known, B can be uniquely determined.

Example:

student_id → student_name


📌 Functional dependencies are the foundation of normalization.

2️⃣ First Normal Form (1NF)

Rule:

Each field contains atomic (indivisible) values

No repeating groups or multi-valued attributes

❌ Not in 1NF
STUDENT(id, name, courses)
101, Harsh, DBMS, OS

✅ In 1NF
STUDENT(id, name)
ENROLLMENT(id, course)


📌 Key idea: One cell = one value

3️⃣ Second Normal Form (2NF)

Rule:

Table must be in 1NF

No partial dependency on a composite primary key

📌 Applies only when composite keys exist

❌ Violation Example

Primary key: (student_id, course_id)

student_id, course_id → student_name


Here, student_name depends only on student_id.

✅ Fix

Split into:

STUDENT(student_id, student_name)

ENROLLMENT(student_id, course_id)

📌 Key idea:

No attribute should depend on part of a composite key.

4️⃣ Third Normal Form (3NF)

Rule:

Table must be in 2NF

No transitive dependency

Transitive dependency:

A → B → C

❌ Violation Example
student_id → dept_id
dept_id → dept_name


So:

student_id → dept_name (indirect)

✅ Fix

Split into:

STUDENT(student_id, dept_id)

DEPARTMENT(dept_id, dept_name)

📌 Key idea:

Non-key attributes should depend only on the primary key.

5️⃣ BCNF (Boyce–Codd Normal Form) – Basic Idea

Stronger version of 3NF

Rule:

For every functional dependency A → B, A must be a super key

📌 Handles rare edge cases where 3NF still allows redundancy.

You usually don’t design directly for BCNF unless needed.

Bad vs Good Design (Quick Contrast)
❌ Bad Design
STUDENT(id, name, course, instructor)


Repeated instructor names

Update anomalies

✅ Good Design
STUDENT(id, name)
COURSE(course_id, course_name, instructor)
ENROLLMENT(id, course_id)

🧠 Interview Gold Nuggets

1NF → atomic values

2NF → no partial dependency

3NF → no transitive dependency

BCNF → every determinant is a super key

Normalization improves consistency, not performance