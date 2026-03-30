
# 🟢 2. Relation (Core Structure) + 🔑 Keys

## 📌 Relation (Table)

A **Relation** is a table used to store data in rows and columns.

### ✅ Example:

| Student_ID | Name  | Email            |
|------------|-------|------------------|
| 1          | Kunal | k@abc.com        |
| 2          | Amit  | a@abc.com        |

---

## 📌 Tuple (Row) & Attribute (Column)

- **Tuple** → A single row in a table  
- **Attribute** → A column in a table  

### ✅ Example:

| Student_ID | Name  | Email |
|------------|-------|-------|

👉 Attributes: Student_ID, Name, Email  
👉 Tuple: (1, Kunal, k@abc.com)

---

## 📌 Degree & Cardinality

- **Degree** → Number of columns  
- **Cardinality** → Number of rows  

### ✅ Example:

| ID | Name  | Dept |
|----|-------|------|
| 1  | A     | IT   |
| 2  | B     | HR   |

👉 Degree = 3  
👉 Cardinality = 2  

---

# 🔑 Types of Keys

Keys are used to **identify rows uniquely** and **maintain relationships**.

---

## 🔹 Basic Keys

### 📌 Super Key
A **Super Key** is any set of attributes that can uniquely identify a row.

### ✅ Example:
- {Student_ID}
- {Student_ID, Name}

👉 Both can identify a row → both are Super Keys

---

### 📌 Candidate Key
A **Candidate Key** is a **minimal Super Key** (no extra attribute).

### ✅ Example:
- Student_ID ✔
- Email ✔ (if unique)

👉 Both are Candidate Keys

---

### 📌 Primary Key
A **Primary Key** is the selected Candidate Key used to uniquely identify rows.

### Rules:
- Cannot be NULL  
- Must be unique  

### ✅ Example:
```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50)
);
````

---

### 📌 Alternate Key

Candidate Keys that are **not chosen as Primary Key**

### ✅ Example:

* Candidate Keys: Student_ID, Email
* Primary Key: Student_ID
  👉 Email = Alternate Key

---

## 🔹 Relational Key

### 📌 Foreign Key

A **Foreign Key** is used to create a relationship between two tables.

### ✅ Example:

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);

CREATE TABLE marks (
    student_id INT,
    marks INT,
    FOREIGN KEY (student_id) REFERENCES students(id)
);
```

👉 `student_id` in marks = Foreign Key

---

## 🔹 Structural Keys

### 📌 Composite Key

A key made of **two or more attributes**

### ✅ Example:

* (Student_ID, Course_ID)

```sql
PRIMARY KEY (student_id, course_id)
```

---

### 📌 Simple Key

A key consisting of **only one attribute**

👉 Example:

* Student_ID

---

## 🔹 Special Keys

### 📌 Unique Key

Ensures all values are **unique** (NULL allowed sometimes)

```sql
email VARCHAR(50) UNIQUE
```

---

### 📌 Natural Key

A key derived from **real-world data**

👉 Example:

* Email
* Aadhaar number

---

### 📌 Surrogate Key

Artificial key created by system

👉 Example:

* Auto-increment ID

```sql
id INT AUTO_INCREMENT PRIMARY KEY
```

---

### 📌 Secondary Key

A non-unique key used for **searching/filtering**

👉 Example:

* Department (many students can have same)

---

## ✅ Mini Solved Example

### 🎯 Problem:

Identify keys in this table:

| ID | Email                             | Name |
| -- | --------------------------------- | ---- |
| 1  | [a@gmail.com](mailto:a@gmail.com) | A    |
| 2  | [b@gmail.com](mailto:b@gmail.com) | B    |

### ✅ Solution:

* Super Keys → {ID}, {Email}, {ID, Name}
* Candidate Keys → ID, Email
* Primary Key → ID
* Alternate Key → Email

---

## ⚠️ Common Mistakes

* Super Key ≠ Candidate Key
* Primary Key = only ONE (per table)
* Foreign Key can have duplicates ✔
* Composite Key = multiple columns

---

## 🧠 Quick Revision

* Relation = Table
* Tuple = Row
* Attribute = Column
* Degree = Columns
* Cardinality = Rows

### Keys:

* Super → Any unique combination
* Candidate → Minimal
* Primary → Selected
* Foreign → Relationship
* Composite → Multiple columns

---

## 📝 Practice Questions

* [ ] Define Relation, Tuple, Attribute
* [ ] Find Degree & Cardinality
* [ ] Differentiate Super Key & Candidate Key
* [ ] Identify keys from given table
* [ ] Write SQL for Primary & Foreign Key

---

##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---


