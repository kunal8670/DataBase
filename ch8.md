
# 🟢 8. Aggregation


## 📌 Overview

Aggregation means **combining multiple rows into a single result** using functions like:
- COUNT()
- SUM()
- AVG()
- MAX()
- MIN()

👉 Usually used with `GROUP BY`

---

# 🟢 1. GROUP BY Concept

Used to **group rows based on a column**

---

## 💻 Example Table

| name  | department | salary |
|-------|------------|--------|
| A     | IT         | 50000  |
| B     | IT         | 60000  |
| C     | HR         | 40000  |

---

## 💻 Query

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
````

---

## 🎯 Output

| department | avg_salary |
| ---------- | ---------- |
| IT         | 55000      |
| HR         | 40000      |

---

## 📌 Key Points

* Groups rows with same value
* Must use with aggregate functions
* Every selected column must be:

  * In GROUP BY OR
  * Used with aggregate function

---

# 🟢 2. HAVING vs WHERE

---

## 📌 WHERE

* Filters rows
* Works **before grouping**
* Cannot use aggregate functions

---

## 📌 HAVING

* Filters groups
* Works **after GROUP BY**
* Can use aggregate functions

---

## 💻 Example

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;
```

---

## 🎯 Output

| department | avg_salary |
| ---------- | ---------- |
| IT         | 55000      |

---

## 🔄 Comparison Table

| Feature           | WHERE           | HAVING         |
| ----------------- | --------------- | -------------- |
| Filters           | Rows            | Groups         |
| Execution         | Before GROUP BY | After GROUP BY |
| Aggregate allowed | ❌ No            | ✅ Yes          |

---

# 🟢 3. Aggregation with Multiple Columns

Used when grouping by more than one column

---

## 💻 Example Table

| name | dept | city   | salary |
| ---- | ---- | ------ | ------ |
| A    | IT   | Pune   | 50000  |
| B    | IT   | Pune   | 60000  |
| C    | IT   | Mumbai | 70000  |
| D    | HR   | Pune   | 40000  |

---

## 💻 Query

```sql
SELECT dept, city, AVG(salary)
FROM employees
GROUP BY dept, city;
```

---

## 🎯 Output

| dept | city   | avg_salary |
| ---- | ------ | ---------- |
| IT   | Pune   | 55000      |
| IT   | Mumbai | 70000      |
| HR   | Pune   | 40000      |

---

## 📌 Key Points

* Groups based on **combination of columns**
* Each unique combination forms a group

---

## ✅ Mini Solved Example

### 🎯 Problem:

Find departments with more than 2 employees

---

### 💻 Solution

```sql
SELECT department, COUNT(*) AS total
FROM employees
GROUP BY department
HAVING COUNT(*) > 2;
```

---

### 🧠 Logic

* GROUP BY → group employees
* COUNT → count rows
* HAVING → filter groups

---

## ⚠️ Common Mistakes

* Using WHERE instead of HAVING ❌
* Missing GROUP BY column in SELECT ❌
* Using non-aggregated column without GROUP BY ❌

---

## 🧠 Quick Revision

* GROUP BY → group rows
* HAVING → filter groups
* WHERE → filter rows

---

## 📝 Practice Questions

* [ ] Write GROUP BY query
* [ ] Difference between WHERE and HAVING
* [ ] Aggregate multiple columns
* [ ] Count rows per group

---

