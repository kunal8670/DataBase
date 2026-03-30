
# 🟢 1. Introduction to Database & SQL

## 📌 What is Database

A **Database** is an organized collection of data stored in a structured way so it can be easily accessed, managed, and updated.

### ✅ Example (Real-life)
Think of a **college system**:

| Student_ID | Name  | Branch |
|------------|-------|--------|
| 1          | Kunal | CSE    |
| 2          | Amit  | IT     |

👉 This table = **Database (collection of data)**

---

## 📌 What is DBMS

**DBMS (Database Management System)** is software used to create, manage, and interact with databases.

### 🔹 Examples:
- :contentReference[oaicite:0]{index=0}  
- :contentReference[oaicite:1]{index=1}  
- :contentReference[oaicite:2]{index=2}  

### ✅ Responsibilities of DBMS:
- Store data
- Retrieve data
- Update/Delete data
- Security & backup

---

## 📌 What is RDBMS

**RDBMS (Relational DBMS)** stores data in the form of **tables (relations)** and maintains relationships between them.

### 🔹 Key Idea:
👉 Data is stored in **rows + columns**

---

## 🔄 DBMS vs RDBMS

| Feature        | DBMS                     | RDBMS                         |
|---------------|--------------------------|--------------------------------|
| Structure     | File-based / simple      | Table-based (relations)        |
| Relationships | Not supported            | Supported (via keys)           |
| Data Integrity| Low                      | High                           |
| Examples      | File system              | MySQL, PostgreSQL              |

---

## 📌 Features of RDBMS

- [ ] Data stored in tables (relations)
- [ ] Supports relationships (Foreign Key)
- [ ] Data integrity & constraints
- [ ] Reduces redundancy
- [ ] Supports SQL queries
- [ ] Multi-user access
- [ ] Security & backup

---

## 📌 What is SQL

**SQL (Structured Query Language)** is used to interact with databases.

👉 Used to:
- Create tables
- Insert data
- Retrieve data
- Update/Delete data

---

## 💻 Basic SQL Example

```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50),
    branch VARCHAR(10)
);

INSERT INTO students VALUES (1, 'Kunal', 'CSE');

SELECT * FROM students;
````

---

## 📌 Real-world Applications of SQL

### 🏦 Banking System

* Store customer data
* Track transactions

### 🛒 E-commerce (Amazon/Flipkart)

* Products database
* Orders & payments

### 🎓 College Systems

* Student records
* Marks & attendance

### 📱 Social Media

* User profiles
* Posts & messages

---

## ✅ Mini Solved Example

### 🎯 Problem:

Store employee data and retrieve employees from IT department.

```sql
CREATE TABLE employees (
    id INT,
    name VARCHAR(50),
    department VARCHAR(20)
);

INSERT INTO employees VALUES
(1, 'Kunal', 'IT'),
(2, 'Amit', 'HR');

SELECT * FROM employees
WHERE department = 'IT';
```

### ✅ Output:

| id | name  | department |
| -- | ----- | ---------- |
| 1  | Kunal | IT         |

---

## 🧠 Quick Revision

* Database = Collection of data
* DBMS = Software to manage database
* RDBMS = Table-based DBMS with relations
* SQL = Language to interact with DB

---

## 📝 Practice Questions

* [ ] Define Database and DBMS
* [ ] Difference between DBMS and RDBMS
* [ ] Write 2 real-world uses of SQL
* [ ] Write a SQL query to create a table

---

##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---


