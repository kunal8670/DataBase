
# 🟢 7. Functions



## 📌 Overview

Functions are used to **perform operations on data**.

👉 Two main types:
- Aggregate Functions → operate on multiple rows  
- Scalar Functions → operate on single values  

---

# 🟢 Aggregate Functions

Used to perform calculations on a **set of rows**

---

## 📌 1. COUNT()

Returns number of rows

---

### 💻 Example

```sql
SELECT COUNT(*) FROM students;
````

👉 Counts all rows

---

### 📌 With Condition

```sql id="2ozf8r"
SELECT COUNT(*) FROM students
WHERE marks > 70;
```

---

---

## 📌 2. SUM()

Returns total sum

---

### 💻 Example

```sql id="9snr1p"
SELECT SUM(marks) FROM students;
```

---

---

## 📌 3. AVG()

Returns average value

---

### 💻 Example

```sql id="s3w8y6"
SELECT AVG(marks) FROM students;
```

---

---

## 📌 4. MAX()

Returns maximum value

---

### 💻 Example

```sql id="3y79dj"
SELECT MAX(marks) FROM students;
```

---

---

## 📌 5. MIN()

Returns minimum value

---

### 💻 Example

```sql id="t1r2rj"
SELECT MIN(marks) FROM students;
```

---

## ⚠️ Important Notes

* Ignore NULL values
* Used with GROUP BY for grouping
* Cannot be used in WHERE (use HAVING)

---

# 🟢 Scalar Functions

Operate on **individual values**

---

## 📌 1. UPPER()

Converts text to uppercase

---

### 💻 Example

```sql id="v3snyp"
SELECT UPPER(name) FROM students;
```

---

---

## 📌 2. LOWER()

Converts text to lowercase

---

### 💻 Example

```sql id="99l41t"
SELECT LOWER(name) FROM students;
```

---

---

## 📌 3. LENGTH()

Returns length of string

---

### 💻 Example

```sql id="r2b5k3"
SELECT LENGTH(name) FROM students;
```

---

---

## 📌 4. ROUND()

Rounds numeric value

---

### 💻 Example

```sql id="y9dc94"
SELECT ROUND(AVG(marks), 2) FROM students;
```

---

## 💻 Combined Example

```sql id="hsmn1n"
SELECT 
    COUNT(*) AS total_students,
    AVG(marks) AS avg_marks,
    MAX(marks) AS highest_marks
FROM students;
```

---

## ✅ Mini Solved Example

### 🎯 Problem:

Find average marks of students scoring above 60

---

### 💻 Solution

```sql id="a6q8d1"
SELECT AVG(marks) 
FROM students
WHERE marks > 60;
```

---

### 🧠 Logic

* WHERE → filter rows
* AVG → calculate average

---

## ⚠️ Common Mistakes

* Using aggregate in WHERE ❌
* Forgetting GROUP BY
* Confusing COUNT(*) vs COUNT(column)
* Ignoring NULL behavior

---

## 🧠 Quick Revision

### Aggregate:

* COUNT → number of rows
* SUM → total
* AVG → average
* MAX → highest
* MIN → lowest

### Scalar:

* UPPER → uppercase
* LOWER → lowercase
* LENGTH → string length
* ROUND → rounding

---

## 📝 Practice Questions

* [ ] Count total records
* [ ] Find average value
* [ ] Use MAX and MIN
* [ ] Convert text case
* [ ] Combine multiple functions

---

##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---

