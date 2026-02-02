🔹 MODULE 9: Subqueries & Views

Goal: Write advanced queries and simplify complex logic

1️⃣ Subqueries (Nested Queries)

A subquery is a query written inside another query.

📌 Used when the result of one query is needed by another.

Key points:

Executed before the outer query

Can return:

Single value

Multiple values

Can appear in:

WHERE

FROM

SELECT

2️⃣ Correlated Subqueries

A correlated subquery depends on the outer query.

📌 It is executed once for each row of the outer query.

Why important:

More powerful

Usually slower than normal subqueries

📌 Interview line:

A correlated subquery cannot run independently.

3️⃣ IN vs EXISTS (Very Important)
IN

Compares a value with a list of values

Subquery is executed once

📌 Slower for large datasets

EXISTS

Checks whether subquery returns any row

Stops execution as soon as a match is found

📌 Faster for large datasets

📌 Interview rule of thumb:

Use EXISTS for large tables, IN for small results.

4️⃣ Views

A view is a virtual table based on a query.

📌 Stores the query, not the data

Why views are used:

Simplify complex queries

Improve readability

Enhance security

Example View
CREATE VIEW active_users AS
SELECT * FROM users WHERE status = 'active';


📌 Acts like a table but pulls live data.