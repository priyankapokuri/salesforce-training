# Salesforce Summer Program – Day 9

## Component Communication

### Types of Communication

### a) Parent → Child

* Uses `@api` decorator
* Parent passes data via attributes

### b) Child → Parent

* Uses Custom Events
* Child dispatches an event and the parent listens to it

### c) Unrelated Components

* Use Pub-Sub Model or Lightning Message Service (LMS)

---

## Dashboard Architecture

### a) Student Dashboard

#### Components

* StudentProfile
* CourseList
* AttendanceView

### b) Faculty Dashboard

#### Components

* FacultyProfile
* StudentList
* AttendanceUpdater

### c) Admin Dashboard

#### Components

* UserManagement
* CourseManagement
* Reports

### d) Component Communication

* StudentProfile ↔ CourseList (Data Display)
* Faculty → AttendanceUpdater (Updates Data)
* Admin → All Components (Control and Monitoring)

### Components Communicate Using

* Props (`@api`)
* Events
* Shared Services (Apex/LMS)

---

## Data Flow Explanation (Student Registration)

### Flow

```text
UI → Validation → Flow → Apex → Database → Notification
```

### Step-by-Step Process

#### a) UI

* User fills the registration form

#### b) Validation

* Check required fields
* Validate email format

#### c) Flow (LWC Logic)

* Data is prepared and structured

#### d) Apex

* Apex class processes the request
* Business logic is applied

#### e) Database

* Record is stored in Salesforce Object

#### f) Notification

* Success message displayed
* Email confirmation sent

---

## Aura vs LWC – Why Salesforce Moved to LWC

| Feature        | Aura                             | LWC                                                   |
| -------------- | -------------------------------- | ----------------------------------------------------- |
| Performance    | Slower due to framework overhead | Faster using native JavaScript and browser APIs       |
| Architecture   | Framework-heavy and proprietary  | Based on modern web standards (HTML, CSS, JavaScript) |
| Learning Curve | Complex and harder to learn      | Easier and familiar to web developers                 |
| Debugging      | Difficult to debug               | Easier with standard browser developer tools          |

### Why Salesforce Prefers LWC

* Better performance
* Modern architecture
* Easier maintenance
* Faster development
* Improved developer experience

---

## Reflection: Modular Architecture

### Why Do Enterprise Applications Need Modular Design?

* Reusability of components
* Easy maintenance
* Better scalability
* Independent development
* Faster debugging

### Conclusion

Modular architecture allows enterprise applications to be developed using small, reusable, and independent components. This approach improves maintainability, reduces development effort, and enables teams to scale applications efficiently while ensuring a consistent user experience.
