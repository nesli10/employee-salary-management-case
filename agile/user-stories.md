# User Stories

## Employee Salary Management System

---

## 🧩 Epic 1: Salary Management

### US-01: Create Salary Record

**As a** HR Specialist
**I want to** create a salary record for an employee
**So that** employee salary information is stored in the system

**Acceptance Criteria:**

* Salary record can be created with employee ID
* Salary amount must be greater than 0
* Currency must be selected
* Record is saved successfully

---

### US-02: Update Salary

**As a** HR Specialist
**I want to** update an employee’s salary
**So that** changes can be reflected in the system

**Acceptance Criteria:**

* Existing salary can be updated
* Previous salary must be stored in history
* Update must include timestamp and user
* Salary cannot be negative

---

### US-03: View Salary History

**As a** HR Specialist
**I want to** view salary history
**So that** I can track past changes

**Acceptance Criteria:**

* All historical salary records are displayed
* Each record includes old and new values
* Includes timestamp and user information

---

## 🔐 Epic 2: Access Control

### US-04: Role-Based Access

**As a** System Admin
**I want to** restrict access based on roles
**So that** only authorized users can manage salary data

**Acceptance Criteria:**

* Only HR role can create/update salary
* Unauthorized users cannot access salary data
* System returns error for unauthorized access

---

## 🔄 Epic 3: Payroll Integration

### US-05: Send Data to Payroll

**As a** Finance System
**I want to** receive salary data
**So that** payroll processing can be completed

**Acceptance Criteria:**

* Salary data is sent via API
* Data format is correct (JSON)
* System handles failed requests

---

## 📊 Epic 4: Audit & Logging

### US-06: Audit Logs

**As a** Compliance Officer
**I want to** view audit logs
**So that** I can ensure system compliance

**Acceptance Criteria:**

* All actions are logged
* Logs include user and timestamp
* Logs cannot be modified
