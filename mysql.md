# MySQL Study Guide

## 🧩 Beginner Level

- **Q:** What is MySQL?  
  **A:** An open-source relational database management system (RDBMS) that stores and retrieves data using SQL.

- **Q:** What is SQL?  
  **A:** Structured Query Language — used to manage and query relational databases.

- **Q:** What is a primary key?  
  **A:** A unique identifier for each record in a table; cannot be NULL or duplicated.

- **Q:** What is a foreign key?  
  **A:** A column that establishes a relationship between two tables by referencing another table’s primary key.

- **Q:** What is the difference between `CHAR` and `VARCHAR`?  
  **A:** `CHAR` has a fixed length; `VARCHAR` has a variable length.

- **Q:** What are the different types of joins in MySQL?  
  **A:** `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL OUTER JOIN` (emulated), and `CROSS JOIN`.

- **Q:** What is normalization?  
  **A:** The process of organizing data to reduce redundancy and improve integrity.

- **Q:** What are the normal forms?  
  **A:**

  - 1NF: No repeating groups, atomic values
  - 2NF: 1NF + no partial dependency
  - 3NF: 2NF + no transitive dependency

- **Q:** What is denormalization?  
  **A:** Combining tables or duplicating data to improve read performance.

- **Q:** What is the difference between `DELETE`, `TRUNCATE`, and `DROP`?  
  **A:**

  - `DELETE`: removes rows (can use WHERE, logs each row)
  - `TRUNCATE`: removes all rows, faster, resets AUTO_INCREMENT
  - `DROP`: deletes the entire table schema

- **Q:** What are indexes?  
  **A:** Data structures that speed up lookups on columns.

- **Q:** What is the default storage engine in MySQL?  
  **A:** InnoDB (supports transactions, foreign keys, and row-level locking).

- **Q:** How do you create a new database and table?  
   **A:**
  ```sql
  CREATE DATABASE app_db;
  USE app_db;
  CREATE TABLE users (id INT PRIMARY KEY AUTO_INCREMENT, name VARCHAR(100));
  ```

## ⚙️ Intermediate Level

- **Q:** What is a composite key?
  **A:** A primary key made up of multiple columns.

- **Q:** What is the difference between WHERE and HAVING?
  **A:** WHERE filters rows before aggregation; HAVING filters after aggregation.

- **Q:** What is an alias in SQL?
  **A:** A temporary name for a table or column using AS.

- **Q:** What does GROUP BY do?
  **A:** Groups rows with the same values into summary rows (used with aggregate functions).

- **Q:** What are aggregate functions?
  **A:** COUNT(), SUM(), AVG(), MIN(), MAX() — used with GROUP BY.

- **Q:** How do transactions work in MySQL?
  **A:** A set of SQL operations that execute as a single unit using START TRANSACTION, COMMIT, or ROLLBACK.

- **Q:** What is ACID compliance?
  **A:**

> Atomicity: all-or-nothing
> Consistency: maintains valid state
> Isolation: transactions don’t interfere
> Durability: committed data persists

- **Q:** What is a subquery?
  **A:** A query nested inside another SQL statement.

- **Q:** What is a self-join?
  **A:** Joining a table to itself using aliases.

- **Q:** What are views?
  **A:** Virtual tables defined by queries; simplify complex joins.

- **Q:** What are stored procedures?
  **A:** Precompiled SQL routines that can take parameters and return results.

- **Q:** What is the difference between a stored procedure and a function?
  **A:** A function returns a value; a procedure can return multiple results and modify data.

- **Q:** What is a trigger?
  **A:** A function automatically executed in response to certain database events (e.g., AFTER INSERT).

- **Q:** What are foreign key constraints used for?
  **A:** Enforce referential integrity between tables.

- **Q:** How do you optimize a slow query?
  **A:** Use indexes, avoid SELECT \*, analyze EXPLAIN plans, and minimize joins/subqueries.

- **Q:** What is EXPLAIN used for?
  **A:** Displays how MySQL executes a query (indexes used, join types, etc.).

## 🧠 Advanced Level

- **Q:** What is the difference between clustered and non-clustered indexes?
  **A:**

> Clustered: actual data stored in index order (InnoDB’s primary key).
> Non-clustered: separate structure pointing to data rows.

- **Q:** What are common index types in MySQL?
  **A:** BTREE (default), HASH (MEMORY engine), and FULLTEXT.

- **Q:** What is query caching?
  **A:** Caches results of queries to speed up repeated executions (deprecated in modern MySQL).

- **Q:** What are isolation levels in MySQL?
  **A:**

  > READ UNCOMMITTED
  > READ COMMITTED
  > REPEATABLE READ (default)
  > SERIALIZABLE

- **Q:** What is the difference between optimistic and pessimistic locking?
  **A:**

  > Optimistic: assume no conflicts; check before commit
  > Pessimistic: lock resources early to prevent conflicts

- **Q:** What are deadlocks and how do you prevent them?
  **A:** Circular waits between transactions — prevent by consistent update order and shorter transactions.

- **Q:** How do you design a many-to-many relationship?
  **A:** Use a junction table with two foreign keys referencing the related tables.

- **Q:** What is the difference between INNER JOIN and LEFT JOIN performance-wise?
  **A:** LEFT JOIN may process more rows due to including non-matching data.

- **Q:** What is a covering index?
  **A:** An index that contains all the columns a query needs — no table access required.

- **Q:** How does InnoDB differ from MyISAM?
  **A:** InnoDB supports ACID, transactions, foreign keys, and row-level locks; MyISAM does not.

- **Q:** What are some strategies for scaling MySQL?
  **A:**

  > Vertical scaling (bigger servers)
  > Horizontal scaling (sharding, replication)
  > Caching (Redis, Memcached)

- **Q:** What is replication in MySQL?
  **A:** Copying data from a master to one or more replicas for redundancy or load balancing.

- **Q:** What is the difference between master-slave and master-master replication?
  **A:**

  > Master-slave: one-way replication
  > Master-master: bi-directional replication (both writable)

- **Q:** How does indexing affect INSERT/UPDATE performance?
  **A:** Speeds up reads but can slow down writes due to index maintenance.

- **Q:** What are the advantages of using prepared statements?
  **A:** Prevent SQL injection and improve performance for repeated queries.

- **Q:** How can you detect and fix slow queries?
  **A:** Use the slow query log and EXPLAIN ANALYZE to optimize.

- **Q:** What is partitioning?
  **A:** Splitting large tables into smaller physical parts to improve query performance and maintenance.

- **Q:** How do transactions interact with auto-increment columns?
  **A:** InnoDB reserves IDs even for rolled-back transactions, creating gaps.
