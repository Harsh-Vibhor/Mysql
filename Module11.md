🔹 MODULE 11: Transactions & ACID Properties

Goal: Ensure data safety and consistency

What is a Transaction?

A transaction is a sequence of operations executed as a single logical unit.

📌 Either all succeed or all fail.

ACID Properties
Atomicity

All operations succeed or none do

Consistency

Database moves from one valid state to another

Isolation

Transactions don’t interfere with each other

Durability

Once committed, data is permanent

📌 ACID ensures reliable transactions.

Concurrency Problems (Conceptual)
Dirty Read

Reading uncommitted data

Lost Update

One update overwrites another

Phantom Read

New rows appear during a transaction

📌 Solved using isolation levels (awareness only).