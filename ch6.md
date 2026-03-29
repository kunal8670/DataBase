
# 🟢 6. Clauses (Query Structure)

## 📌 Overview

Clauses define **how a SQL query behaves**.

👉 Standard query flow:

```sql
SELECT column
FROM table
WHERE condition
GROUP BY column
HAVING condition
ORDER BY column;
````

---

# 🟢 1. SELECT

Used to **choose columns**

---

### 💻 Example

```sql
SELECT name, marks FROM students;
```

---

### 📌 Notes

* `*` → selects all columns
* Can select specific columns

---

# 🟢 2. FROM

Specifies the **table**

---

### 💻 Example

```sql
SELECT * FROM students;
```

---

# 🟢 3. WHERE

Filters rows **before grouping**

---

### 💻 Example

```sql id="qlow9j"
SELECT * FROM students
WHERE marks > 70;
```

---

### 📌 Important

* Cannot use aggregate functions here

---

# 🟢 4. ORDER BY

Sorts the result

---

### 💻 Example

```sql id="m7r7l4"
SELECT * FROM students
ORDER BY marks DESC;
```

---

### 📌 Options

* ASC (default)
* DESC

---

# 🟢 5. GROUP BY

Groups rows for aggregation

---

### 💻 Example

```sql id="y9zjfx"
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```

---

# 🟢 6. HAVING

Filters groups **after GROUP BY**

---

### 💻 Example

```sql id="6j1i7n"
SELECT department, AVG(salary)
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;
```

---

### 📌 Difference

| WHERE           | HAVING         |
| --------------- | -------------- |
| Filters rows    | Filters groups |
| Before GROUP BY | After GROUP BY |

---

# 🔗 Logical Operators

Used to combine conditions

---

## 🟢 AND

Both conditions must be true

```sql id="n5m9zx"
SELECT * FROM students
WHERE marks > 70 AND branch = 'CSE';
```

---

## 🟢 OR

At least one condition must be true

```sql id="7oqvks"
SELECT * FROM students
WHERE marks > 80 OR branch = 'IT';
```

---

## 🟢 NOT

Negates condition

```sql id="d9u0px"
SELECT * FROM students
WHERE NOT branch = 'CSE';
```

---

# 🔍 Comparison Operators

---

## 🟢 Basic Operators

```sql
= , != , > , < , >= , <=
```

---

### 💻 Example

```sql id="rfj0ob"
SELECT * FROM students
WHERE marks >= 75;
```

---

## 🟢 BETWEEN

Range condition

```sql id="6g9l2d"
SELECT * FROM students
WHERE marks BETWEEN 60 AND 80;
```

---

## 🟢 IN

Match multiple values

```sql id="6o17n9"
SELECT * FROM students
WHERE branch IN ('CSE', 'IT');
```

---

## 🟢 LIKE

Pattern matching

```sql id="br0b64"
SELECT * FROM students
WHERE name LIKE 'K%';
```

👉 Starts with 'K'

---

## 🟢 IS NULL

Check for NULL values

```sql id="q6plq1"
SELECT * FROM students
WHERE email IS NULL;
```

---

## ✅ Mini Solved Example

### 🎯 Problem:

Find students from CSE with marks > 70, sorted by marks

---

### 💻 Solution

```sql id="3sm0y8"
SELECT * FROM students
WHERE branch = 'CSE' AND marks > 70
ORDER BY marks DESC;
```

---

### 🧠 Logic

* WHERE → filter rows
* AND → combine conditions
* ORDER BY → sort

---

## ⚠️ Common Mistakes

* Using HAVING instead of WHERE ❌
* Using aggregate in WHERE ❌
* Forgetting ORDER BY direction
* Confusing AND vs OR

---

## 🧠 Quick Revision

* SELECT → choose columns
* FROM → table
* WHERE → filter rows
* GROUP BY → group data
* HAVING → filter groups
* ORDER BY → sort

---

## 📝 Practice Questions

* [ ] Write query using WHERE
* [ ] Use AND & OR together
* [ ] Use GROUP BY + HAVING
* [ ] Use LIKE and IN
* [ ] Sort data using ORDER BY

---

