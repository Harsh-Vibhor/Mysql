🔹 MODULE 10: Indexing & Performance Basics

Goal: Understand how databases make queries fast

What is an Index?

An index is a data structure that allows the database to find rows faster.

📌 Similar to an index in a book.

How Index Works (Conceptual)

Without index → full table scan

With index → quick lookup (usually B-Tree)

📌 Index stores:

column value → row location

Pros of Indexing

Faster SELECT queries

Efficient filtering and joins

Cons of Indexing

Slower INSERT / UPDATE / DELETE

Extra storage space

When NOT to Use Index

Small tables

Columns with low uniqueness

Frequently updated columns

📌 Interview line:

Index improves read performance but slows down writes.