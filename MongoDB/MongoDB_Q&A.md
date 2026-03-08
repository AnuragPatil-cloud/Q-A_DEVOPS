# 🗄 MySQL Interview Questions & Answers (DevOps)

This section contains commonly asked **MySQL interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is MySQL?

MySQL is an **open-source relational database management system (RDBMS)** used to store and manage structured data.

It uses **SQL (Structured Query Language)** to manage data.

---

# 2. What is a Database?

A database is an **organized collection of data stored electronically** so it can be accessed, managed, and updated easily.

Example:

- User data
- Application logs
- Product information

---

# 3. What is SQL?

SQL (Structured Query Language) is used to **interact with relational databases**.

Operations include:

- Creating tables
- Inserting data
- Updating data
- Deleting data
- Querying data

---

# 4. What are the main SQL commands?

Types of SQL commands:

DDL (Data Definition Language)

```
CREATE
ALTER
DROP
```

DML (Data Manipulation Language)

```
INSERT
UPDATE
DELETE
```

DQL (Data Query Language)

```
SELECT
```

DCL (Data Control Language)

```
GRANT
REVOKE
```

---

# 5. What is a Table?

A table is a **collection of rows and columns used to store data** in a database.

Example table:

```
Users
-------------------------
ID | Name | Email
```

---

# 6. What is a Primary Key?

A primary key is a **column that uniquely identifies each record in a table**.

Example:

```
ID INT PRIMARY KEY
```

---

# 7. What is a Foreign Key?

A foreign key is used to **link two tables together**.

Example:

```
FOREIGN KEY (user_id) REFERENCES users(id)
```

---

# 8. What is Normalization?

Normalization is the process of **organizing database tables to reduce redundancy and improve data integrity**.

Common normal forms:

- 1NF
- 2NF
- 3NF

---

# 9. What is an Index?

An index improves **database query performance by speeding up data retrieval**.

Example:

```
CREATE INDEX idx_name ON users(name);
```

---

# 10. What is a JOIN?

JOIN is used to **combine rows from two or more tables** based on a related column.

Types of joins:

- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN

Example:

```
SELECT users.name, orders.order_id
FROM users
INNER JOIN orders
ON users.id = orders.user_id;
```

---

# 11. What is a View?

A view is a **virtual table created from a query**.

Example:

```
CREATE VIEW active_users AS
SELECT * FROM users WHERE status='active';
```

---

# 12. What is a Stored Procedure?

A stored procedure is a **predefined SQL code stored in the database that can be executed when needed.**

---

# 13. What is Replication in MySQL?

Replication allows **data from one database server to be copied to another server automatically**.

Types:

- Master-Slave replication
- Master-Master replication

Benefits:

- High availability
- Load balancing
- Backup

---

# 14. What is MySQL Backup?

Backup is the process of **creating copies of database data to prevent data loss**.

Example command:

```
mysqldump -u root -p database_name > backup.sql
```

Restore backup:

```
mysql -u root -p database_name < backup.sql
```

---

# 15. What is a Transaction?

A transaction is a **set of database operations executed as a single unit**.

ACID properties:

- Atomicity
- Consistency
- Isolation
- Durability

---

# 16. What is MySQL Port?

Default MySQL port:

```
3306
```

---

# 17. How do you connect to MySQL?

Example command:

```
mysql -u root -p
```

---

# 18. How do you list databases in MySQL?

```
SHOW DATABASES;
```

---

# 19. How do you list tables in a database?

```
SHOW TABLES;
```

---

# 20. Real DevOps Scenario

### Problem

Application cannot connect to MySQL database.

### Solution

Check:

1. MySQL service status

```
systemctl status mysql
```

2. MySQL port

```
3306
```

3. Firewall rules

4. Database credentials

---

# 🚀 Why MySQL is Important for DevOps

DevOps engineers often manage databases for applications.

MySQL is used for:

- Application data storage
- Logging
- Backend services
- Monitoring systems

MySQL integrates with:

- AWS RDS
- Kubernetes
- Docker
- CI/CD pipelines
