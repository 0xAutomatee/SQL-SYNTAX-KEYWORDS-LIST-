# MS SQL Server Basic Keywords Grouped by Use Case + Sample Syntax

Total Basic Keywords: **82**

> Note: Some keywords are used in `SELECT` queries, some in table creation, some in transactions, and some in control flow.  
> So, all 82 basic keywords cannot naturally fit into one simple `SELECT` query, but they can be used in one SQL Server script/batch.

---

# 1. Data Selection Keywords

Used to read data from tables.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 1 | SELECT | Select columns/data | `SELECT column_name` |
| 2 | FROM | Used after SELECT to choose table | `SELECT * FROM table_name` |
| 3 | WHERE | Filter records | `WHERE age > 18` |
| 4 | DISTINCT | Remove duplicate rows | `SELECT DISTINCT city FROM users` |
| 5 | TOP | Limit number of rows | `SELECT TOP 10 * FROM users` |
| 6 | ORDER | Sort records | `ORDER BY name` |
| 7 | BY | Used with ORDER/GROUP | `ORDER BY name` |
| 8 | ASC | Sort ascending | `ORDER BY name ASC` |
| 9 | DESC | Sort descending | `ORDER BY id DESC` |
| 10 | GROUP | Group rows | `GROUP BY city` |
| 11 | HAVING | Filter grouped data | `HAVING COUNT(*) > 1` |
| 12 | ALL | Compare with all values | `> ALL (SELECT salary FROM staff)` |
| 13 | ANY | Compare with any value | `> ANY (SELECT salary FROM staff)` |

---

# 2. Filtering and Conditions

Used to create conditions in queries.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 14 | AND | Multiple conditions | `WHERE age > 18 AND city = 'Lahore'` |
| 15 | OR | Alternative condition | `WHERE city = 'Lahore' OR city = 'Karachi'` |
| 16 | NOT | Reverse condition | `WHERE NOT city = 'Lahore'` |
| 17 | IN | Match multiple values | `WHERE city IN ('Lahore', 'Karachi')` |
| 18 | BETWEEN | Match range | `WHERE age BETWEEN 18 AND 30` |
| 19 | LIKE | Pattern matching | `WHERE name LIKE 'A%'` |
| 20 | IS | Used with NULL | `WHERE name IS NULL` |
| 21 | NULL | Empty/unknown value | `WHERE email IS NULL` |
| 22 | EXISTS | Check if subquery returns rows | `WHERE EXISTS (SELECT 1 FROM orders)` |

---

# 3. Joins

Used to combine data from multiple tables.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 23 | JOIN | Combine tables | `FROM users JOIN orders` |
| 24 | INNER | Inner join | `INNER JOIN orders ON users.id = orders.user_id` |
| 25 | LEFT | Left join | `LEFT JOIN orders ON users.id = orders.user_id` |
| 26 | RIGHT | Right join | `RIGHT JOIN orders ON users.id = orders.user_id` |
| 27 | FULL | Full join | `FULL JOIN orders ON users.id = orders.user_id` |
| 28 | OUTER | Outer join | `FULL OUTER JOIN orders ON users.id = orders.user_id` |
| 29 | ON | Join condition | `ON users.id = orders.user_id` |
| 30 | UNION | Combine result sets | `SELECT name FROM users UNION SELECT name FROM customers` |

---

# 4. Table and Database Creation

Used to create or change database objects.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 31 | CREATE | Create object | `CREATE TABLE users` |
| 32 | ALTER | Modify object | `ALTER TABLE users ADD age INT` |
| 33 | DROP | Delete object | `DROP TABLE users` |
| 34 | DATABASE | Create/use database | `CREATE DATABASE SchoolDB` |
| 35 | TABLE | Create table | `CREATE TABLE students` |
| 36 | COLUMN | Refer to table column | `ALTER TABLE students ADD COLUMN_NAME INT` |
| 37 | ADD | Add column/constraint | `ALTER TABLE students ADD age INT` |
| 38 | CONSTRAINT | Add rule | `CONSTRAINT PK_students PRIMARY KEY (id)` |
| 39 | PRIMARY | Primary key | `PRIMARY KEY (id)` |
| 40 | FOREIGN | Foreign key | `FOREIGN KEY (dept_id)` |
| 41 | KEY | Used with primary/foreign | `PRIMARY KEY (id)` |
| 42 | CHECK | Validation condition | `CHECK (age >= 18)` |
| 43 | DEFAULT | Default value | `DEFAULT 0` |
| 44 | UNIQUE | Unique values | `UNIQUE (email)` |
| 45 | INDEX | Create index | `CREATE INDEX idx_name ON users(name)` |
| 46 | VIEW | Create view | `CREATE VIEW v_users AS SELECT * FROM users` |
| 47 | FUNCTION | Create function | `CREATE FUNCTION fn_test()` |
| 48 | PROCEDURE | Create stored procedure | `CREATE PROCEDURE sp_test AS SELECT 1` |
| 49 | TRIGGER | Create trigger | `CREATE TRIGGER trg_test ON users AFTER INSERT AS SELECT 1` |

---

# 5. Data Modification

Used to insert, update, and delete data.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 50 | INSERT | Insert data | `INSERT INTO users` |
| 51 | INTO | Used with INSERT | `INSERT INTO users(name)` |
| 52 | VALUES | Insert values | `VALUES ('Ali')` |
| 53 | UPDATE | Update records | `UPDATE users SET name = 'Ali'` |
| 54 | DELETE | Delete records | `DELETE FROM users WHERE id = 1` |
| 55 | TRUNCATE | Remove all rows | `TRUNCATE TABLE users` |
| 56 | SET | Assign value | `SET name = 'Ali'` |
| 57 | USE | Select database | `USE SchoolDB` |

---

# 6. Transactions

Used to manage save/rollback of changes.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 58 | BEGIN | Start block/transaction | `BEGIN TRAN` |
| 59 | COMMIT | Save transaction | `COMMIT TRAN` |
| 60 | ROLLBACK | Undo transaction | `ROLLBACK TRAN` |
| 61 | TRAN | Short form of transaction | `BEGIN TRAN` |
| 62 | TRANSACTION | Full form | `BEGIN TRANSACTION` |

---

# 7. Variables and Control Flow

Used in SQL logic and programming.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 63 | DECLARE | Declare variable | `DECLARE @age INT` |
| 64 | IF | Conditional logic | `IF @age > 18 SELECT 'Adult'` |
| 65 | ELSE | Alternative condition | `ELSE SELECT 'Minor'` |
| 66 | WHILE | Loop | `WHILE @i < 10` |
| 67 | CASE | Conditional expression | `CASE WHEN age > 18 THEN 'Adult' END` |
| 68 | WHEN | Used inside CASE | `WHEN age > 18` |
| 69 | THEN | Used inside CASE | `THEN 'Adult'` |
| 70 | END | End CASE/block | `END` |
| 71 | PRINT | Print message | `PRINT 'Done'` |
| 72 | EXEC | Execute procedure | `EXEC sp_name` |
| 73 | EXECUTE | Execute procedure | `EXECUTE sp_name` |
| 74 | RETURN | Return from procedure/function | `RETURN` |

---

# 8. System/User Keywords

Used for current user, date, and system values.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 75 | CURRENT | Current value/context | `CURRENT_TIMESTAMP` |
| 76 | CURRENT_DATE | Current date | `CURRENT_DATE` |
| 77 | CURRENT_TIME | Current time | `CURRENT_TIME` |
| 78 | CURRENT_TIMESTAMP | Current date and time | `CURRENT_TIMESTAMP` |
| 79 | USER | Current database user | `SELECT USER` |

---

# 9. Other Basic Keywords

Common supporting keywords.

| SR# | Keyword | Use Case | Syntax Example |
|---:|---|---|---|
| 80 | AS | Alias name | `SELECT name AS student_name` |
| 81 | TO | Used in permissions / logic | `GRANT SELECT TO user_name` |
| 82 | WITH | Used with CTE/options | `WITH cte AS (...) SELECT * FROM cte` |

---

# Sample SQL Server Script Using All 82 Basic Keywords

```sql
-- USE
USE tempdb;

-- CREATE, DATABASE
-- CREATE DATABASE DemoKeywordDB;

-- DROP, TABLE
IF OBJECT_ID('dbo.BasicOrders', 'U') IS NOT NULL
    DROP TABLE dbo.BasicOrders;

IF OBJECT_ID('dbo.BasicUsers', 'U') IS NOT NULL
    DROP TABLE dbo.BasicUsers;

-- CREATE, TABLE, PRIMARY, KEY, UNIQUE, DEFAULT, CHECK, CONSTRAINT, FOREIGN, COLUMN/ADD through ALTER
CREATE TABLE dbo.BasicUsers
(
    UserID INT NOT NULL,
    UserName VARCHAR(50) NOT NULL,
    City VARCHAR(50) DEFAULT 'Unknown',
    Age INT NULL,
    Email VARCHAR(100) UNIQUE,
    CONSTRAINT PK_BasicUsers PRIMARY KEY (UserID),
    CONSTRAINT CK_BasicUsers_Age CHECK (Age IS NULL OR Age BETWEEN 1 AND 120)
);

CREATE TABLE dbo.BasicOrders
(
    OrderID INT NOT NULL PRIMARY KEY,
    UserID INT NOT NULL,
    Amount DECIMAL(10,2) DEFAULT 0,
    CONSTRAINT FK_BasicOrders_Users FOREIGN KEY (UserID)
        REFERENCES dbo.BasicUsers(UserID)
);

-- ALTER, ADD
ALTER TABLE dbo.BasicUsers
ADD StatusName VARCHAR(20) DEFAULT 'Active';

-- INSERT, INTO, VALUES
INSERT INTO dbo.BasicUsers
    (UserID, UserName, City, Age, Email)
VALUES
    (1, 'Ali', 'Lahore', 22, 'ali@example.com'),
    (2, 'Sara', 'Karachi', 25, 'sara@example.com'),
    (3, 'Ahmed', NULL, NULL, 'ahmed@example.com');

INSERT INTO dbo.BasicOrders
    (OrderID, UserID, Amount)
VALUES
    (101, 1, 500),
    (102, 1, 700),
    (103, 2, 300);

-- CREATE, INDEX
CREATE INDEX IX_BasicUsers_UserName
ON dbo.BasicUsers(UserName);

-- DECLARE, SET
DECLARE @MinAge INT;
SET @MinAge = 18;

-- BEGIN, TRAN, TRANSACTION, COMMIT, ROLLBACK
BEGIN TRAN;
UPDATE dbo.BasicUsers
SET City = 'Islamabad'
WHERE UserID = 3;

COMMIT TRAN;

BEGIN TRANSACTION;
UPDATE dbo.BasicUsers
SET City = 'Temporary'
WHERE UserID = 3;

ROLLBACK TRANSACTION;

-- IF, ELSE, PRINT
IF EXISTS (SELECT 1 FROM dbo.BasicUsers WHERE Age IS NOT NULL)
    PRINT 'Users found';
ELSE
    PRINT 'No users found';

-- WHILE
DECLARE @Counter INT;
SET @Counter = 1;

WHILE @Counter <= 1
BEGIN
    PRINT 'Loop running';
    SET @Counter = @Counter + 1;
END;

-- WITH, AS, SELECT, TOP, DISTINCT, FROM, JOIN, INNER, LEFT, RIGHT, FULL, OUTER, ON,
-- WHERE, AND, OR, NOT, IN, BETWEEN, LIKE, IS, NULL, EXISTS,
-- GROUP, BY, HAVING, ORDER, ASC, DESC,
-- CASE, WHEN, THEN, END,
-- ALL, ANY, CURRENT, CURRENT_DATE, CURRENT_TIME, CURRENT_TIMESTAMP, USER
WITH UserCTE AS
(
    SELECT
        UserID,
        UserName AS NameAlias,
        City,
        Age,
        CASE
            WHEN Age >= @MinAge THEN 'Adult'
            ELSE 'Minor or Unknown'
        END AS AgeGroup,
        CURRENT_TIMESTAMP AS CurrentDateTimeValue,
        CURRENT_USER AS CurrentUserValue,
        USER AS DatabaseUserValue
    FROM dbo.BasicUsers
)
SELECT DISTINCT TOP 10
    u.UserID,
    u.NameAlias AS UserName,
    u.City,
    u.Age,
    u.AgeGroup,
    o.Amount,
    CURRENT_TIMESTAMP AS CurrentTimestampExample
FROM UserCTE AS u
INNER JOIN dbo.BasicOrders AS o
    ON u.UserID = o.UserID
LEFT JOIN dbo.BasicOrders AS lo
    ON u.UserID = lo.UserID
RIGHT JOIN dbo.BasicOrders AS ro
    ON u.UserID = ro.UserID
FULL OUTER JOIN dbo.BasicOrders AS fo
    ON u.UserID = fo.UserID
WHERE
    u.Age IS NOT NULL
    AND u.Age BETWEEN 18 AND 60
    AND u.City IN ('Lahore', 'Karachi', 'Islamabad')
    AND u.NameAlias LIKE 'A%'
    OR NOT EXISTS
    (
        SELECT 1
        FROM dbo.BasicOrders AS x
        WHERE x.UserID = u.UserID
    )
    AND o.Amount >= ALL
    (
        SELECT Amount
        FROM dbo.BasicOrders
        WHERE Amount IS NOT NULL
    )
    OR o.Amount > ANY
    (
        SELECT Amount
        FROM dbo.BasicOrders
        WHERE Amount IS NOT NULL
    )
GROUP BY
    u.UserID,
    u.NameAlias,
    u.City,
    u.Age,
    u.AgeGroup,
    o.Amount
HAVING COUNT(*) >= 1
ORDER BY
    u.NameAlias ASC,
    o.Amount DESC;

-- UNION
SELECT UserName AS ResultName
FROM dbo.BasicUsers
UNION
SELECT City AS ResultName
FROM dbo.BasicUsers
WHERE City IS NOT NULL;

-- CREATE, VIEW
EXEC('
CREATE VIEW dbo.vBasicUsers
AS
SELECT UserID, UserName, City
FROM dbo.BasicUsers
');

-- CREATE, PROCEDURE
EXEC('
CREATE PROCEDURE dbo.spBasicUsers
AS
BEGIN
    SELECT * FROM dbo.BasicUsers;
    RETURN;
END
');

-- EXEC, EXECUTE
EXEC dbo.spBasicUsers;
EXECUTE dbo.spBasicUsers;

-- CREATE, FUNCTION
EXEC('
CREATE FUNCTION dbo.fnBasicNumber()
RETURNS INT
AS
BEGIN
    RETURN 1;
END
');

-- CREATE, TRIGGER
EXEC('
CREATE TRIGGER dbo.trgBasicUsers
ON dbo.BasicUsers
AFTER INSERT
AS
BEGIN
    PRINT ''Trigger executed'';
END
');

-- DELETE
DELETE FROM dbo.BasicOrders
WHERE OrderID = 103;

-- TRUNCATE
TRUNCATE TABLE dbo.BasicOrders;

-- DROP
DROP TRIGGER dbo.trgBasicUsers;
DROP FUNCTION dbo.fnBasicNumber;
DROP PROCEDURE dbo.spBasicUsers;
DROP VIEW dbo.vBasicUsers;
DROP TABLE dbo.BasicOrders;
DROP TABLE dbo.BasicUsers;
