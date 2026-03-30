
# 🟢 9. Joins (Very Important)



## 📌 Overview

Joins are used to **combine data from multiple tables** based on a related column.

👉 Mostly based on:
- Primary Key
- Foreign Key

---

## 💻 Example Tables

### students

| id | name  |
|----|-------|
| 1  | Kunal |
| 2  | Amit  |
| 3  | Ravi  |

---

### marks

| student_id | marks |
|------------|-------|
| 1          | 80    |
| 2          | 70    |
| 4          | 60    |

---

# 🟢 1. INNER JOIN

Returns only **matching rows**

---

### 💻 Query

```sql
SELECT s.name, m.marks
FROM students s
INNER JOIN marks m
ON s.id = m.student_id;
````

---

### 🎯 Output

| name  | marks |
| ----- | ----- |
| Kunal | 80    |
| Amit  | 70    |

---

## 📌 Use Case

* Get common data between tables

---

# 🟢 2. LEFT JOIN (LEFT OUTER JOIN)

Returns all rows from left table + matched rows from right

---

### 💻 Query

```sql id="7e6l5b"
SELECT s.name, m.marks
FROM students s
LEFT JOIN marks m
ON s.id = m.student_id;
```

---

### 🎯 Output

| name  | marks |
| ----- | ----- |
| Kunal | 80    |
| Amit  | 70    |
| Ravi  | NULL  |

---

---

# 🟢 3. RIGHT JOIN (RIGHT OUTER JOIN)

Returns all rows from right table + matched rows from left

---

### 💻 Query

```sql id="s9w9sq"
SELECT s.name, m.marks
FROM students s
RIGHT JOIN marks m
ON s.id = m.student_id;
```

---

### 🎯 Output

| name  | marks |
| ----- | ----- |
| Kunal | 80    |
| Amit  | 70    |
| NULL  | 60    |

---

---

# 🟢 4. FULL JOIN (FULL OUTER JOIN)

Returns all rows from both tables

---

### 💻 Query

```sql id="8v5qj1"
SELECT s.name, m.marks
FROM students s
FULL JOIN marks m
ON s.id = m.student_id;
```

---

### 🎯 Output

| name  | marks |
| ----- | ----- |
| Kunal | 80    |
| Amit  | 70    |
| Ravi  | NULL  |
| NULL  | 60    |

---

---

# 🟢 5. CROSS JOIN

Returns **all combinations (Cartesian product)**

---

### 💻 Query

```sql id="h3zq9y"
SELECT s.name, m.marks
FROM students s
CROSS JOIN marks m;
```

---

### 📌 Result

* If students = 3 rows
* marks = 3 rows

👉 Output = 3 × 3 = 9 rows

---

---

# 🟢 6. SELF JOIN

Table joined with itself

---

### 💻 Example (Employee Manager)

| id | name | manager_id |
| -- | ---- | ---------- |
| 1  | A    | NULL       |
| 2  | B    | 1          |

---

### 💻 Query

```sql id="n4f1k2"
SELECT e.name AS employee, m.name AS manager
FROM employees e
LEFT JOIN employees m
ON e.manager_id = m.id;
```

---

---

# 🟢 7. NATURAL JOIN

Automatically joins on columns with same name

---

### 💻 Query

```sql id="ndtpxl"
SELECT * FROM students
NATURAL JOIN marks;
```

---

### ⚠️ Note

* No ON condition needed
* Rarely used in real projects

---

# 🟢 8. EQUI JOIN

Join using `=` condition

---

### 💻 Example

```sql id="u8ntmr"
SELECT *
FROM students s, marks m
WHERE s.id = m.student_id;
```

👉 Same as INNER JOIN

---

---

# 🟢 9. NON-EQUI JOIN

Join using conditions like >, <, BETWEEN

---

### 💻 Example

| marks | grade |
| ----- | ----- |
| 80    | A     |
| 70    | B     |

---

```sql id="i7a5gd"
SELECT s.name, g.grade
FROM students s
JOIN grades g
ON s.marks BETWEEN g.min_marks AND g.max_marks;
```

---

---

## ✅ Mini Solved Example

### 🎯 Problem:

Find all students with or without marks

---

### 💻 Solution

```sql id="e4pxtd"
SELECT s.name, m.marks
FROM students s
LEFT JOIN marks m
ON s.id = m.student_id;
```

---

---

## ⚠️ Common Mistakes

* Missing JOIN condition ❌
* Using wrong JOIN type ❌
* Confusing LEFT vs RIGHT ❌
* Using CROSS JOIN accidentally ❌

---

## 🧠 Quick Revision

* INNER → only matching
* LEFT → all left + match
* RIGHT → all right + match
* FULL → everything
* CROSS → all combinations
* SELF → same table
* NATURAL → auto match
* EQUI → = condition
* NON-EQUI → range condition

---

## 📝 Practice Questions

* [ ] Write INNER JOIN query
* [ ] Difference LEFT vs RIGHT
* [ ] Find unmatched rows
* [ ] Use SELF JOIN
* [ ] Use NON-EQUI JOIN

---

##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---



