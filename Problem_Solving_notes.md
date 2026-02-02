🧾 SQL Quick Reference (Problem-Solving Notes)
🔹 Query Modifiers

Sort results → ORDER BY

Limit number of rows → LIMIT

Remove duplicates → DISTINCT

Filter within a range (inclusive) → BETWEEN x AND y

🔹 Pattern Matching (Strings)

Match pattern → LIKE

Exclude pattern → NOT LIKE

Wildcard

% → any number of characters

_ → exactly one character

🔹 Aggregate Functions

Count rows → COUNT(column)
(COUNT(*) counts all rows)

Sum values → SUM(column)

Average → AVG(column)

Maximum value → MAX(column)

Minimum value → MIN(column)

🔹 Numeric Functions

Round value → ROUND(number, decimals)

Floor (largest integer ≤ value) → FLOOR(number)

Ceil (smallest integer ≥ value) → CEIL(number)

Absolute value → ABS(number)

Power → POWER(value, exponent)

Square root → SQRT(number)

🔹 String Functions

Length of string → LENGTH(string)

Concatenate strings → CONCAT(str1, str2)

First n characters → LEFT(string, n)

Last n characters → RIGHT(string, n)

Replace substring → REPLACE(input, 'old', 'new')

📌 Example: remove all 0s

REPLACE(input, '0', '')

🔹 Date Function

Extract year from date → YEAR(date_column)

🔹 Conditional Logic (CASE)
CASE
  WHEN condition THEN result
  WHEN condition THEN result
  ELSE result
END


📌 Used for conditional columns.

🔹 Multiple JOIN Syntax
SELECT columns
FROM table1
JOIN table2 ON condition1
JOIN table3 ON condition2
JOIN table4 ON condition3;


📌 Joins are evaluated left to right.

🧠 Final Tip (Very Important)

While problem solving, always think:

Row-level filter → WHERE

Group-level filter → HAVING

Calculation across rows → Aggregate function

Conditional output → CASE