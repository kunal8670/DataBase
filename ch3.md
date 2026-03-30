
# 🟢 3. Domain (Data Rules)


## 📌 Domain Definition

A **Domain** is the **set of valid values** that an attribute (column) can take.

👉 It defines:
- Type of data
- Range of values
- Rules for valid input

---

### ✅ Example:

| Age |
|-----|
| 21  |
| 25  |

👉 Domain of Age:
- Must be integer  
- Cannot be negative  

---

## 📌 Why Domain is Important

- Ensures **data correctness**
- Prevents invalid data entry
- Maintains **data integrity**

---

## 📌 Data Types

Data types define **what kind of data** a column can store.

---

### 🔹 Common Data Types

#### 1. INT
- Stores integers  
- Example: 1, 100, -5  

```sql
age INT
````

---

#### 2. VARCHAR(n)

* Stores variable-length strings
* Example: "Kunal", "Hello"

```sql
name VARCHAR(50)
```

---

#### 3. DATE

* Stores date values
* Format: 'YYYY-MM-DD'

```sql
dob DATE
```

---

#### 4. FLOAT

* Stores decimal numbers

```sql
salary FLOAT
```

---

## 💻 Example Table with Data Types

```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50),
    dob DATE,
    marks FLOAT
);
```

---

## 📌 Constraints

Constraints are rules applied on columns to **restrict invalid data**.

---

### 🔹 1. NOT NULL

* Column cannot have NULL value

```sql
name VARCHAR(50) NOT NULL
```

👉 ❌ Invalid:

```sql
INSERT INTO students (id) VALUES (1);
```

---

### 🔹 2. UNIQUE

* All values must be different

```sql
email VARCHAR(50) UNIQUE
```

👉 ❌ Duplicate values not allowed

---

### 🔹 3. CHECK

* Restricts values based on condition

```sql
age INT CHECK (age >= 18)
```

👉 Only allows age ≥ 18

---

### 🔹 4. DEFAULT

* Assigns default value if none provided

```sql
country VARCHAR(20) DEFAULT 'India'
```

---

## 💻 Full Example (With Constraints)

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(50) UNIQUE,
    age INT CHECK (age >= 18),
    country VARCHAR(20) DEFAULT 'India'
);
```

---

## ✅ Mini Solved Example

### 🎯 Problem:

Insert valid and invalid data

```sql
INSERT INTO users VALUES (1, 'Kunal', 'k@gmail.com', 21, 'India');
```

✔ Valid

```sql
INSERT INTO users VALUES (2, NULL, 'a@gmail.com', 25, 'India');
```

❌ Invalid → NOT NULL violation

```sql
INSERT INTO users VALUES (3, 'Amit', 'k@gmail.com', 22, 'India');
```

❌ Invalid → UNIQUE violation

---

## ⚠️ Common Mistakes

* Using wrong data type (e.g., storing numbers in VARCHAR)
* Forgetting constraints
* Assuming NULL = 0 ❌
* Ignoring CHECK conditions

---

## 🧠 Quick Revision

* Domain = Valid set of values
* Data Types = Type of data stored
* Constraints = Rules for data validation

### Constraints:

* NOT NULL → No empty value
* UNIQUE → No duplicates
* CHECK → Condition-based
* DEFAULT → Auto value

---

## 📝 Practice Questions

* [ ] Define Domain with example
* [ ] Explain INT vs VARCHAR
* [ ] Write SQL with constraints
* [ ] Identify constraint violations

---

##### © 2026 Kunal Harshad Patil  
For more learning resources and updates, connect with me:  
[GitHub](https://github.com/kunal8670) • [LinkedIn](https://www.linkedin.com/in/kunal-patil-8733b528a/)

---



