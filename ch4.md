
# 🟢 4. Types of SQL (5 Categories)

---

## 📌 Overview

SQL commands are divided into **5 categories** based on their function.

| Type | Full Form | Purpose |
|------|----------|--------|
| DDL  | Data Definition Language | Define structure |
| DML  | Data Manipulation Language | Modify data |
| DQL  | Data Query Language | Retrieve data |
| DCL  | Data Control Language | Control access |
| TCL  | Transaction Control Language | Manage transactions |

---

# 🟢 1. DDL (Data Definition Language)

Used to **define or modify database structure**

### 🔹 Commands:
- CREATE
- ALTER
- DROP

---

### 💻 Examples

#### CREATE
```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50)
);
````

---

#### ALTER

```sql
ALTER TABLE students ADD age INT;
```

---

#### DROP

```sql
DROP TABLE students;
```

---

### ⚠️ Important Points

* Changes structure permanently
* Auto-commit (cannot rollback in most DBs)

---

# 🟢 2. DML (Data Manipulation Language)

Used to **insert, update, delete data**

### 🔹 Commands:

* INSERT
* UPDATE
* DELETE

---

### 💻 Examples

#### INSERT

```sql
INSERT INTO students VALUES (1, 'Kunal');
```

---

#### UPDATE

```sql
UPDATE students
SET name = 'Amit'
WHERE id = 1;
```

---

#### DELETE

```sql
DELETE FROM students
WHERE id = 1;
```

---

### ⚠️ Important Points

* Affects data, not structure
* Can be rolled back (with transactions)

---

# 🟢 3. DQL (Data Query Language)

Used to **retrieve data**

### 🔹 Command:

* SELECT

---

### 💻 Example

```sql
SELECT * FROM students;
```

---

### 🔍 With Condition

```sql
SELECT name FROM students
WHERE id = 1;
```

---

# 🟢 4. DCL (Data Control Language)

Used to **control access/permissions**

### 🔹 Commands:

* GRANT
* REVOKE

---

### 💻 Examples

#### GRANT

```sql
GRANT SELECT ON students TO user1;
```

---

#### REVOKE

```sql
REVOKE SELECT ON students FROM user1;
```

---

# 🟢 5. TCL (Transaction Control Language)

Used to **manage transactions**

---

## 📌 What is Transaction?

A **transaction** is a group of SQL operations executed together.

---

### 🔹 Commands:

* COMMIT
* ROLLBACK
* SAVEPOINT

---

### 💻 Examples

#### COMMIT

```sql
COMMIT;
```

---

#### ROLLBACK

```sql
ROLLBACK;
```

---

#### SAVEPOINT

```sql
SAVEPOINT sp1;
```

---

### ✅ Mini Example (Transaction)

```sql
INSERT INTO students VALUES (1, 'Kunal');
SAVEPOINT s1;

INSERT INTO students VALUES (2, 'Amit');

ROLLBACK TO s1;
```

👉 Result:

* Only first insert is saved

---

## ⚠️ Common Mistakes

* Confusing DML with DDL
* Thinking SELECT is DML ❌
* Forgetting COMMIT after transaction
* Assuming DROP can be rolled back ❌

---

## 🧠 Quick Revision

* DDL → Structure
* DML → Data change
* DQL → Data fetch
* DCL → Permissions
* TCL → Transactions

---

## 📝 Practice Questions

* [ ] Define all 5 types of SQL
* [ ] Write 2 commands of each type
* [ ] Difference between DDL and DML
* [ ] What is transaction?

---
