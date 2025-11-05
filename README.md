Servlet and JSP Based Web Application Project Overview

This project demonstrates three core modules using Java Servlets, JSP, and JDBC integration with a MySQL database. It covers:

User Login System

Displaying Employee Records from Database

Student Attendance Portal

Each module follows the MVC (Model–View–Controller) pattern for better structure and maintainability.

📁 Project Structure ServletJSPProject/ │ ├── WebContent/ │ ├── login.html │ ├── attendance.jsp │ ├── WEB-INF/ │ │ └── web.xml │ └── src/ ├── LoginServlet.java ├── EmployeeServlet.java └── AttendanceServlet.java

🧩 Part A — User Login Using Servlet and HTML Form Description:

Implements a simple user authentication system using HTML form and Servlet validation.

Files:

login.html

LoginServlet.java

Logic Flow:

User submits credentials via login.html.

LoginServlet validates username and password.

Displays success or failure message based on match.

Username	Password
admin	1234
🧩 Part B — Display Employee Records with JDBC and Servlet Integration Description:

Fetches and displays all employee records from the MySQL database using JDBC.

Database Schema: CREATE TABLE employees ( id INT PRIMARY KEY, name VARCHAR(50), designation VARCHAR(50), salary DOUBLE );

ogic Flow:

The servlet connects to MySQL using JDBC.

Executes SELECT * FROM employees.

Displays data in HTML table format.

Files:

EmployeeServlet.java

🧩 Part C — Student Attendance Portal Using JSP and Servlet Description:

A simple portal for marking student attendance using a JSP form and storing data in MySQL.

Database Schema: CREATE TABLE attendance ( id INT AUTO_INCREMENT PRIMARY KEY, student_id VARCHAR(10), status VARCHAR(10), date DATE );

Logic Flow:

attendance.jsp collects student ID and attendance status.

AttendanceServlet inserts record into database.

Displays confirmation message on success.

⚙️ Configuration Database Connection

DBMS: MySQL

Username: root

Password: yourpassword

Database Names: company (for employees), college (for attendance)

Driver: com.mysql.cj.jdbc.Driver

web.xml (Servlet Mappings) LoginServlet LoginServlet LoginServlet /LoginServlet

EmployeeServlet EmployeeServlet EmployeeServlet /EmployeeServlet AttendanceServlet AttendanceServlet AttendanceServlet /AttendanceServlet
🚀 How to Run

Install Apache Tomcat and MySQL.

Place project folder inside webapps/ of Tomcat.

Add mysql-connector-j.jar to WEB-INF/lib/.

Configure web.xml with correct servlet mappings.

Start Tomcat server and open in browser:

Login: http://localhost:8080/ServletJSPProject/login.html

Employees: http://localhost:8080/ServletJSPProject/EmployeeServlet

Attendance: http://localhost:8080/ServletJSPProject/attendance.jsp

🧠 Concepts Used

Java Servlets (Request/Response Handling)

JSP (Frontend Integration)

JDBC (Database Connectivity)

MVC Design Pattern

HTML Form Handling

Exception Handling and Data Validation

✅ Output Examples

1️⃣ Login Success

Login Successful!

2️⃣ Employee Records

ID | Name | Designation | Salary
1 | Ayush | Manager | 65000 2 | Riya | Developer | 50000

3️⃣ Attendance Submission

Attendance recorded successfully!

👨‍💻 Developer

Ayush Rana Chandigarh University Department of Computer Science & Engineering
