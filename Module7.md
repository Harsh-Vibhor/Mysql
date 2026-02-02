🔹 MODULE 7: SQL Queries (Core Skills)

Goal: Understand the logic, execution order, and edge cases of SQL queries

🔑 Key Terms You MUST Know (Before Anything Else)
Logical Query Execution Order (Very Important)

SQL is not executed top-to-bottom.

Actual order:

FROM

WHERE

GROUP BY

HAVING

SELECT

ORDER BY

LIMIT

📌 This explains why some queries behave “weirdly”.

1️⃣ WHERE

Purpose: Filter rows before grouping

Works on individual rows

Cannot use aggregate functions

📌 Happens before GROUP BY

Key term: Row-level filtering

2️⃣ GROUP BY

Purpose: Group rows that share the same values

Used with aggregate functions

Every selected column must be:

In GROUP BY, or

An aggregate

📌 Creates groups, not rows

Key term: Grouping attribute

3️⃣ HAVING

Purpose: Filter groups after aggregation

Works on aggregated data

Can use aggregate functions

📌 Happens after GROUP BY

Key term: Group-level filtering

🧠 WHERE vs HAVING (Classic Interview Question)
Feature	WHERE	HAVING
Filters	Rows	Groups
Uses aggregates	❌ No	✅ Yes
Execution time	Before GROUP BY	After GROUP BY

4️⃣ ORDER BY

Purpose: Sort the result set

ASC (default)

DESC

📌 Happens after SELECT

Key terms:

Sorting

Result set ordering

5️⃣ LIMIT

Purpose: Restrict number of rows returned

📌 Applied after sorting

Key term: Pagination

6️⃣ Aggregate Functions
Aggregate functions are SQL functions that perform a calculation on a set of rows and return a single value.

📌 They summarize data, not row-by-row — they work on a group of rows.

Common Aggregate Functions
1️⃣ COUNT()

Counts the number of rows.

COUNT(*) → counts all rows (including NULLs)

COUNT(column) → counts only non-NULL values

📌 Very common interview trap.

2️⃣ SUM()

Adds up numeric values in a column.

Ignores NULL values

Works only on numeric data

3️⃣ AVG()

Calculates the average of numeric values.

Ignores NULL values

4️⃣ MIN()

Returns the smallest value.

Works with numbers, dates, strings

5️⃣ MAX()

Returns the largest value.

Works with numbers, dates, strings

🧠 High-Value Edge Cases (These Matter)
NULL Behavior

Aggregates ignore NULL (except COUNT(*))

WHERE column = NULL ❌ wrong

Use IS NULL

GROUP BY with Multiple Columns

Groups by unique combinations

Order of columns matters logically

HAVING Without GROUP BY?

Allowed in SQL

Treated as filtering aggregated result

📌 Rare but interviewer-favorite trick