# College Management System using Salesforce Concepts

## 1. Difference Between App, Object, Record, and Field

| Concept | Description | Example in College Management System |
|---|---|---|
| App | A collection of related tools, tabs, and features created for a specific purpose | College Administration App |
| Object | A storage structure similar to a database table that stores related data | Student Object, Faculty Object |
| Record | A single entry stored inside an object | Information of one student |
| Field | A single data value inside a record | Student Name, Email, Department |

---

# 2. Standard Objects vs Custom Objects

| Standard Objects | Custom Objects |
|---|---|
| Objects already available in Salesforce | Objects created by users based on requirements |
| Used for common CRM activities | Used for organization-specific processes |
| Cannot be removed permanently | Can be modified or deleted |
| Examples: Account, Contact, Opportunity | Examples: Student, Course, Faculty |
| Provided by default in Salesforce | Designed manually according to business needs |

---

# 3. College Management Data Model

## Student Object
Stores information related to students.

### Fields
- Student ID
- First Name
- Last Name
- Email Address
- Phone Number
- Department
- Course

---

## Faculty Object
Maintains faculty-related details.

### Fields
- Faculty ID
- Faculty Name
- Email Address
- Department
- Subject Expertise

---

## Course Object
Stores details about courses offered in the institution.

### Fields
- Course ID
- Course Name
- Total Seats
- Available Seats
- Assigned Faculty
- Department

---

## Department Object
Maintains department information.

### Fields
- Department ID
- Department Name
- HOD Name

---

# Relationships Between Objects

| Parent Object | Child Object | Relationship Type |
|---|---|---|
| Department | Student | One-to-Many |
| Department | Faculty | One-to-Many |
| Department | Course | One-to-Many |
| Faculty | Course | One-to-Many |
| Course | Student | One-to-Many |

---

# Data Model Diagram

```text
                     +----------------------+
                     |      Department      |
                     +----------------------+
                     | Department ID        |
                     | Department Name      |
                     | HOD Name             |
                     +----------------------+
                        /        |        \
                       /         |         \
                      /          |          \
         One-to-Many /           |           \ One-to-Many

            +----------------+        +----------------+
            |    Student     |        |    Faculty     |
            +----------------+        +----------------+
            | Student ID     |        | Faculty ID     |
            | Student Name   |        | Faculty Name   |
            | Email          |        | Email          |
            | Phone Number   |        | Specialization |
            | Course ID      |        +----------------+
            | Department ID  |
            +----------------+
                     |
                     |
                     | One-to-Many
                     |
                     v
              +----------------------+
              |        Course        |
              +----------------------+
              | Course ID            |
              | Course Name          |
              | Total Seats          |
              | Available Seats      |
              | Faculty ID           |
              | Department ID        |
              +----------------------+
```

---

# 4. Formula Fields

## Full Name Formula

### Formula
```text
First Name + " " + Last Name
```

### Explanation
This formula automatically combines the first name and last name to create a complete name. It reduces manual effort and maintains consistency.

---

## Remaining Seats Formula

### Formula
```text
Total Seats - Enrolled Students
```

### Explanation
This formula calculates the number of seats available in a course automatically and helps avoid overbooking.

---

## Percentage Formula

### Formula
```text
(Obtained Marks / Total Marks) * 100
```

### Explanation
This formula automatically calculates the percentage scored by a student, improving accuracy during result preparation.

---

# 5. Validation Rules

## Email Field Validation

### Rule
The email field should not be empty.

### Explanation
This ensures that every student or faculty record contains valid communication information.

---

## Student Age Validation

### Rule
Age must always be greater than zero.

### Explanation
This prevents invalid age values from being entered into the system.

---

## Course Seat Validation

### Rule
Enrolled students should not exceed the total number of seats.

### Explanation
This helps manage classroom capacity properly and avoids admission errors.

---

# 6. Importance of Structured Enterprise Data

Structured enterprise data helps organizations store information in a well-organized and connected format. Instead of managing scattered spreadsheets, institutions can use structured systems to improve efficiency, reduce mistakes, and handle large amounts of data effectively.

In a college management system, structured data helps to:

- Manage students and faculty efficiently
- Connect departments with courses
- Generate reports quickly
- Improve data consistency
- Avoid duplicate records
- Support automation and analytics

With properly connected objects and relationships, organizations can retrieve information easily, maintain accuracy, and make better business decisions.
