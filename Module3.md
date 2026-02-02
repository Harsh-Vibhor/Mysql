🔹 MODULE 3: SQL Language Categories (Very Important)

Goal: Understand types of SQL commands (as expected in interviews)

🟦 1️⃣ DDL – Data Definition Language

Used to define or modify database structure

Commands

CREATE

ALTER

DROP

TRUNCATE

Key Points

Works on schema / structure

Changes are auto-committed

Cannot be rolled back

Example
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(50)
);


📌 TRUNCATE removes all records but keeps table structure.

🟩 2️⃣ DML – Data Manipulation Language

Used to manipulate data inside tables

Commands

INSERT

UPDATE

DELETE

SELECT (see note below)

Key Points

Works on rows

Can be rolled back

Transaction-controlled

Example
INSERT INTO users VALUES (1, 'Harsh');

📌 Important NOTE on SELECT (Interview-Safe)

In many textbooks & interviews, SELECT is considered part of DML

Conceptually, it does not modify data

Some sources define it as DQL, but DQL is usually not counted separately in interviews

👉 Best interview answer:

DML includes INSERT, UPDATE, DELETE, and SELECT.

🟥 3️⃣ DCL – Data Control Language

Used to control access to data

Commands

GRANT

REVOKE

Key Points

Used for authorization

Mostly handled by DBAs

Example (conceptual):

GRANT SELECT ON users TO user1;

🟪 4️⃣ TCL – Transaction Control Language

Purpose: Manage transactions

Commands

COMMIT

ROLLBACK

SAVEPOINT

Key Characteristics

Works only with DML

Ensures data consistency

📌 Simple rule:

COMMIT → save changes

ROLLBACK → undo changes

SAVEPOINT → partial rollback

🧠 Most Important Comparisons (Must Remember)
Operation	Category	Rollback Possible
CREATE	DDL	❌ No
DROP	DDL	❌ No
TRUNCATE	DDL	❌ No
INSERT	DML	✅ Yes
UPDATE	DML	✅ Yes
DELETE	DML	✅ Yes
SELECT	DQL	N/A
🎯 Interview Traps (High Frequency)

TRUNCATE ≠ DELETE

DDL commands auto-commit

TCL works only with DML

SELECT does not modify data