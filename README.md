# 🎓 Comprehensive University Administration Data Model

## 📘 Overview

This project presents a **Comprehensive Data Model** designed for managing and optimizing core academic operations within a university — including **students**, **faculty**, **courses**, and **enrollments**.

Built using **Microsoft SQL Server** and deployed on **Azure SQL Database**, the system simulates a real-world university management environment with a focus on **data integrity**, **query efficiency**, and **scalability**.

---

## 🔧 Technologies Used

- **Microsoft SQL Server (T-SQL)**
- **Azure SQL Database**
- **SSMS (SQL Server Management Studio)**
- **SQL Views, Stored Procedures, User-Defined Functions, Indexing**
- **Joins, Aggregations, String Operations**

---

## ☁️ Cloud Integration

This solution is deployed on an **Azure Cloud SQL Database**, enabling:
- Scalable cloud-based access
- Secure remote querying
- Integration with external dashboards or APIs
- Real-time querying through stored procedures and views

---

## 📂 Schema Overview

### Tables

| Table Name     | Description                                |
|----------------|--------------------------------------------|
| `Students`     | Stores student details (name, DOB, major)  |
| `Faculty`      | Stores faculty profiles and departments    |
| `Courses`      | Course offerings, linked to faculty        |
| `Enrollments`  | Links students and courses with grades     |

---

## 🛠️ Features Implemented

### ✅ Core Functionality

- **Relational Joins** across tables to map students ↔ courses ↔ faculty
- **Stored Procedures** for reusable logic and reporting
- **Scalar Functions** for computing student GPA dynamically
- **Indexed Columns** on high-query tables (e.g., `Enrollments`)
- **Views** for simplifying complex joins for student-course reports

---

## 🔄 Sample Functionality

- ✅ Get all students with enrolled courses and faculty names using a **View**
- ✅ Compute a student's **GPA** using a **User-Defined Scalar Function**
- ✅ Generate performance reports using **Stored Procedures**
- ✅ Optimize queries with **Indexes on Enrollments table**

---

## 📌 Sample T-SQL Queries

```sql
-- Call procedure to fetch student reports
EXEC usp_GetStudentReport;

-- Use scalar function to get GPA
SELECT dbo.GetGPAForStudent(1);

-- Select from view
SELECT * FROM vw_StudentEnrollmentDetails;

![Output1]('/Users/umeaimanmerchant/Desktop/university-db/images/Screenshot 2025-04-12 at 12.38.22 AM.png')
