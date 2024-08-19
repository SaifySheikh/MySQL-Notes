```markdown
# SQL Scripts Repository

This repository contains a collection of SQL scripts organized by different categories, covering basic SQL commands, data types, functions, operators, and constraints. These scripts can be used for learning and practicing SQL concepts.

## Table of Contents

1. [Basics](#basics)
2. [Data Types](#data-types)
3. [Functions](#functions)
4. [Operators](#operators)
5. [Constraints](#constraints)
6. [One-to-many-and-joins](#One-to-many-and-joins)

---

## Basics

**File:** `Basics.sql`

This script covers fundamental SQL commands, including:

- Database operations: `SHOW`, `CREATE`, `DROP`, `USE`.
- Table operations: `CREATE`, `DROP`, `SHOW`, `DESC`.
- Basic `INSERT`, `SELECT`, and filtering operations.

Example:
```sql
-- Create a new database and switch to it
CREATE DATABASE PC;
USE PC;

-- Create a table and insert data
CREATE TABLE GAMES (
    name VARCHAR(50),
    ratings INT
);
INSERT INTO GAMES (name, release_year, ratings)
VALUES ('GTA 6', 2015, 6);
```

## Data Types

**File:** `Datatype.sql`

This script demonstrates how to work with different SQL data types such as `VARCHAR`, `CHAR`, `DATE`, `TIME`, `DATETIME`, and more. It includes examples of creating tables with these data types and inserting data.

Example:
```sql
-- Create a table with different data types
CREATE TABLE events (
    event_name VARCHAR(255),
    event_date DATE,
    event_time TIME,
    event_datetime DATETIME
);
```

## Functions

**File:** `functions.sql`

This script provides examples of various SQL string functions, including `SUBSTRING`, `REPLACE`, `REVERSE`, `CHAR_LENGTH`, `LENGTH`, and more. It also covers `ORDER BY`, `LIMIT`, `COUNT`, and aggregation functions.

Example:
```sql
-- Example of string functions
SELECT REPLACE('Hello World', 'Hello', 'Bye');
SELECT REVERSE('Saify');
```

## Operators

**File:** `operator.sql`

This script demonstrates the use of SQL operators such as comparison operators (`=`, `!=`, `>`, `<`), logical operators (`AND`, `OR`), `BETWEEN`, `IN`, and conditional logic using `CASE`.

Example:
```sql
-- Use of logical operators
SELECT *
FROM Users
WHERE age > 50 AND LENGTH(first_name) > 5;
```

## Constraints

**File:** `constraints.sql`

This script focuses on SQL constraints such as `PRIMARY KEY`, `UNIQUE`, `CHECK`, and how to modify tables using `ALTER`. It includes examples of enforcing data integrity through constraints.

Example:
```sql
-- Create a table with constraints
CREATE TABLE employee (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    emp_age INT CHECK (emp_age >= 18 AND emp_age <= 65),
    emp_salary DECIMAL(10, 2) CHECK (emp_salary >= 0)
);
```

---

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/sql-scripts-repo.git
    ```

2. Navigate to the appropriate directory and execute the SQL scripts in your preferred SQL environment.

3. Modify the scripts according to your needs for learning, practicing, or project use.

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request with improvements or new examples.