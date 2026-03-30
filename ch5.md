
# 🟢 5. Ways of Writing Queries


## 📌 Overview

SQL queries can be written in different ways depending on the problem.

👉 These patterns help you:
- Retrieve data efficiently
- Solve real-world problems
- Prepare for interviews

---

# 🟢 1. Simple Query

A query that retrieves data from a **single table without conditions**

---

### 💻 Example

```sql
SELECT * FROM students;
````

---

### 🎯 Output

| id | name  | marks |
| -- | ----- | ----- |
| 1  | Kunal | 80    |
| 2  | Amit  | 70    |

---

### 📌 Use Case

* View all data
* Basic retrieval

---

# 🟢 2. Conditional Query (WHERE)

Used to filter data based on conditions

---

### 💻 Example

```sql
SELECT * FROM students
WHERE marks > 75;
```

---

### 🎯 Output

| id | name  | marks |
| -- | ----- | ----- |
| 1  | Kunal | 80    |

---

### 📌 Use Case

* Find specific records
* Apply filters

---

# 🟢 3. Join Query

Used to combine data from **multiple tables**

---

### 💻 Example

```sql
SELECT s.name, m.marks
FROM students s
INNER JOIN marks m
ON s.id = m.student_id;
```

---

### 📌 Use Case

* Combine related data
* Real-world databases (orders, users, etc.)

---

# 🟢 4. Subquery (Nested Query)

A query inside another query

---

### 💻 Example

```sql
SELECT name FROM students
WHERE marks > (
    SELECT AVG(marks) FROM students
);
```

---

### 🎯 Logic

1. Inner query → finds average marks
2. Outer query → selects students above average

---

### 📌 Use Case

* Compare with calculated values
* Advanced filtering

---

# 🟢 5. Aggregate Query

Used to perform calculations on multiple rows

---

### 💻 Examples

#### COUNT

```sql
SELECT COUNT(*) FROM students;
```

---

#### AVG

```sql
SELECT AVG(marks) FROM students;
```

---

#### SUM

```sql
SELECT SUM(marks) FROM students;
```

---

### 📌 Use Case

* Reports
* Data analysis

---

## ✅ Mini Solved Example

### 🎯 Problem:

Find students who scored above average marks

---

### 💻 Solution

```sql
SELECT name FROM students
WHERE marks > (
    SELECT AVG(marks) FROM students
);
```

---

### 🧠 Explanation

* Inner query → calculates average
* Outer query → filters based on result

---

## ⚠️ Common Mistakes

* Forgetting WHERE in conditional query
* Wrong JOIN condition → incorrect data
* Subquery returning multiple values unexpectedly
* Using aggregate functions without GROUP BY

---

## 🧠 Quick Revision

* Simple → basic select
* Conditional → WHERE filter
* Join → multiple tables
* Subquery → query inside query
* Aggregate → calculations

---

## 📝 Practice Questions

* [ ] Write a simple SELECT query
* [ ] Use WHERE to filter data
* [ ] Write a JOIN query
* [ ] Write a subquery example
* [ ] Use COUNT and AVG

---
##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---

