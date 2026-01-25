# Zenvy Payroll - Database Schema Design

This document defines the relational structure for the SaaS backend.

## 1. Table: `users`
| Column | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `user_id` | UUID / INT | Primary Key | Unique ID for login |
| `email` | VARCHAR(255) | Unique, Not Null | Login email |
| `password_hash` | TEXT | Not Null | Encrypted password |
| `role` | ENUM | ('Admin', 'HR', 'Employee') | User permissions |

## 2. Table: `employees`
| Column | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `employee_id` | INT | Primary Key | Matches `user_id` |
| `first_name` | VARCHAR(100) | Not Null | |
| `last_name` | VARCHAR(100) | | |
| `department_id` | INT | Foreign Key | Link to Departments table |
| `designation` | VARCHAR(100) | | |
| `joining_date` | DATE | | |
| `base_salary` | DECIMAL(15,2) | | Annual or Monthly base |
| `status` | ENUM | ('Active', 'Inactive') | |

## 3. Table: `attendance`
| Column | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | INT | Primary Key | |
| `employee_id` | INT | Foreign Key | |
| `date` | DATE | | Work date |
| `check_in` | TIME | | |
| `check_out` | TIME | | |
| `overtime_hours`| DECIMAL(4,2) | | |
| `status` | ENUM | ('Present', 'Absent', 'Leave') | |

## 4. Table: `payroll_history`
| Column | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `payroll_id` | INT | Primary Key | |
| `employee_id` | INT | Foreign Key | |
| `month_year` | VARCHAR(10) | | e.g., '01-2024' |
| `gross_salary` | DECIMAL(15,2) | | |
| `tax_deduction` | DECIMAL(15,2) | | |
| `net_salary` | DECIMAL(15,2) | | |
| `payslip_url` | TEXT | | Link to PDF storage |

---

## 5. Relationships (ER Diagram Concept)
*   **One-to-One:** `users` <-> `employees` (Every employee is a user).
*   **One-to-Many:** `employees` -> `attendance` (One employee has many logs).
*   **One-to-Many:** `employees` -> `payroll_history` (Monthly records).
*   **One-to-Many:** `departments` -> `employees`.

## 6. SQL Draft (PostgreSQL/MySQL)
```sql
CREATE TABLE departments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    manager_id INT
);

CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    department_id INT,
    base_salary DECIMAL(10, 2),
    FOREIGN KEY (department_id) REFERENCES departments(id)
);
```
