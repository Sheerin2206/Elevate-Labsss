# 🧑‍💼 Employee Management System (MySQL)

This project is a SQL-based *Employee Management System* that manages employee records, departments, salaries, and attendance. It demonstrates table creation, relationships, constraints, and sample data insertion using MySQL.

---

## 🗂 Database: employee_management_system

---

## 🛠 Tables Created

### 1. employees
Stores core employee information.

| Column            | Type         | Description                  |
|-------------------|--------------|------------------------------|
| emp_id            | INT          | Primary Key                  |
| emp_name          | VARCHAR(50)  | NOT NULL                     |
| emp_email         | VARCHAR(100) | UNIQUE                       |
| emp_age           | INT          | CHECK (≥18) (dropped later)|
| emp_department_id | INT          | Department reference         |
| emp_join_date     | DATE         | Default: CURRENT_DATE        |

---

### 2. salary
Tracks salaries for each employee.

| Column        | Type        | Description                  |
|---------------|-------------|------------------------------|
| emp_id        | INT         | Foreign Key → employees      |
| salary_amnt   | INT         | Salary amount                |
| salary_date   | DATE        | Default: CURRENT_DATE        |

---

### 3. department
Lists departments. (Dropped later)

| Column      | Type         | Description                  |
|-------------|--------------|------------------------------|
| dept_id     | INT          | Primary Key, Auto Increment  |
| dept_name   | VARCHAR(50)  | Department name              |
| location    | VARCHAR(50)  | Default: 'CHENNAI'           |

---

### 4. attendance
Tracks daily attendance of employees.

| Column           | Type        | Description                  |
|------------------|-------------|------------------------------|
| emp_id           | INT         | Foreign Key → employees      |
| attendance_date  | DATE        | Date of attendance           |
| status           | VARCHAR(15) | e.g., present, absent        |

---

## 🔧 Alterations Made

- Dropped emp_age column from employees
- Dropped entire department table

---

## 📥 Sample Data

- *5 employees* added with different departments and emails
- *5 salary records* inserted
- *5 attendance entries* for a specific date
- *5 department records* initially created, then dropped

---

## 🧪 SQL Concepts Used

- CREATE DATABASE, USE
- CREATE TABLE with PRIMARY KEY, FOREIGN KEY, CHECK, and DEFAULT
- INSERT INTO and SELECT
- ALTER TABLE to drop a column
- DROP TABLE to delete a table
- Data types: INT, VARCHAR, DATE

---

## 📌 Execution Flow

1. Database and tables are created.
2. Sample data is inserted into each table.
3. Modifications are made using ALTER and DROP.
4. Data retrieval is done using SELECT * FROM.

---

## 🖼 ER Diagram Suggestion

You can visualize the schema using [dbdiagram.io](https://dbdiagram.io) or MySQL Workbench to understand entity relationships.

---

## 🚀 How to Run

1. Paste the SQL code into MySQL Workbench or any SQL environment.
2. Run the statements in order: database, table creation, inserts, then alterations.
3. Use SELECT queries to verify the results.

---

## 📃 License

This project is open-source and available for educational purposes.

---

✅ Feel free to use or enhance this system for college tasks, demos, or learning SQL!
