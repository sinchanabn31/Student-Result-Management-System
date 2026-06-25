# Student-Result-Management-System # 

A simple "Student Result Management System"developed using "Python" and "MySQL". This project allows users to manage student records, calculate grades, and perform CRUD (Create, Read, Update, Delete) operations through a menu-driven interface.

**Features**
Admin Login
Add Student
View All Students
Search Student by ID
Update Student Details
Delete Student
Automatic Total, Percentage & Grade Calculation
MySQL Database Integration


**Technologies Used**
- Python 3
- MySQL
- MySQL Connector for Python
- Visual Studio Code

---

## Project Structure

Student_Result_Management_System/
│
├── database.py        # Database connection
├── login.py           # Admin login
├── main.py            # Main application
├── README.md



##  Database

### Create Database

```sql
CREATE DATABASE student_db;

USE student_db;

CREATE TABLE students(
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    marks1 INT,
    marks2 INT,
    marks3 INT,
    total INT,
    percentage FLOAT,
    grade CHAR(2)
);
```

### Admin Table

```sql
CREATE TABLE admin(
    username VARCHAR(20),
    password VARCHAR(20)
);

INSERT INTO admin VALUES('admin','admin123');
```

---

##  Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/Student_Result_Management_System.git
```

### Install Required Package

```bash
pip install mysql-connector-python
```

### Configure Database

Open `database.py` and update your MySQL credentials.

```python
connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="YOUR_PASSWORD",
    database="student_db"
)
```

---

##  Run the Project

```bash
python main.py
```

---

##  Sample Output

```
========== ADMIN LOGIN ==========

Enter Username : admin
Enter Password : admin123

Login Successful!

========================================
 STUDENT RESULT MANAGEMENT SYSTEM
========================================

1. Add Student
2. View Students
3. Search Student
4. Update Student
5. Delete Student
6. Exit
```

---

##  Grade Calculation

| Percentage | Grade |
|------------|-------|
| 90 - 100 | A+ |
| 80 - 89 | A |
| 70 - 79 | B |
| 60 - 69 | C |
| 50 - 59 | D |
| Below 50 | F |

---

## Future Enhancements

- GUI using Tkinter
- Export Student Records to CSV
- Student Attendance Module
- Dashboard with Statistics
- Password Encryption
- Web Version using Django or Flask

---

## Author

**Sinchana B N**

- Information Science Engineering Student
- Python | MySQL | DBMS

---

##  License

This project is created for educational and learning purposes.
