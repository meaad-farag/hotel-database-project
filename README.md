

#  Hotel Management System Database Project

##  Project Overview

[cite\_start]This project involves the design, modeling, and implementation of a robust database management system (DBMS) for a hotel and reservation service[cite: 1]. [cite\_start]The primary goal is to simplify office administrative tasks, enhance management functions, and improve the overall experience of customer and guest reservations[cite: 1].

[cite\_start]The system is designed to provide hotel staff with an efficient way to manage core operations, including guest check-ins, check-outs, and reservation confirmation[cite: 1].

##  Technology Stack

| Component | Tool / Language |
| :--- | :--- |
| **DBMS** | [cite\_start]MySQL (Implementation) / SQL Server (Design Mentioned) [cite: 1, 17] |
| **Language** | Structured Query Language (SQL) |
| **Modeling** | Entity-Relationship Diagram (ERD) |
| **Environment** | MySQL Workbench |

##  Key Features & Functionality

The database schema supports the management of all core hotel entities and operations:

  * [cite\_start]**Employee Management:** Tracks detailed information for all hotel employees, including personal details, salary, start date, and gender[cite: 7, 8].
  * [cite\_start]**Department Organization:** Maps employees to various departments and handles the management structure[cite: 5, 6].
  * [cite\_start]**Customer Records:** Stores essential customer information (ID, name, phone number) to facilitate the reservation process[cite: 9].
  * [cite\_start]**Reservation Handling:** Manages all reservation details, including check-in/out dates, payment type, and links to specific rooms and customers[cite: 11, 12].
  * [cite\_start]**Room Inventory:** Maintains records for all rooms, detailing the room number, type, floor number, and price[cite: 13].
  * [cite\_start]**Hotel Identity:** Stores basic hotel information (name, address, phone number)[cite: 4].

##  Database Design

The system was designed using a relational model to ensure data integrity and minimize redundancy.

### 1\. Entity-Relationship Diagram (ERD)

[cite\_start]The ERD visually represents the relationships between the main entities (HOTEL, EMPLOYEE, DEPARTMENT, CUSTOMER, ROOM, RESERVATION) and their attributes[cite: 14].

**(Insert ERD Image Here: The image from source 14)**

### 2\. Database Schema

[cite\_start]The logical schema defines the tables, primary keys, and foreign keys, establishing the relationships that enforce data consistency across the system[cite: 15, 16].

**(Insert Database Schema Image Here: The image from source 15 or 16)**

##  Implementation & SQL Examples

[cite\_start]The database was implemented using **MySQL**[cite: 17]. The following are examples of critical SQL queries used to generate reports for hotel management:

### 1\. Employee Roster and Contact Details

[cite\_start]Retrieving the name, phone number, and salary for all employees[cite: 19].

```sql
SELECT employee.Name, employee.Phone, employee.Salary
FROM hotel.employee;
```

### 2\. Monthly Payroll Cost

[cite\_start]Calculating the total sum of salaries required to run the hotel for one month[cite: 20].

```sql
SELECT sum(employee.Salary)
FROM hotel.employee;
-- Result: 27500
```

### 3\. Employee-Department Mapping

[cite\_start]Joining the `employee` and `department` tables to show which employee works in which department[cite: 21].

```sql
SELECT employee.Name, department.DName
FROM hotel.employee, hotel.department
WHERE employee.EDID = department.DID;
```

-----

##  Prepared By

  * Meaad Farag
