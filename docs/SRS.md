# System Requirements Specification (SRS)

## Employee Salary Management System

---

## 1. Introduction

### 1.1 Purpose

This document defines the system-level requirements for the Employee Salary Management System.
It translates business requirements into detailed technical specifications for development and implementation.

---

### 1.2 Scope

The system will:

* Store and manage employee salary data
* Maintain salary history with versioning
* Provide secure access based on roles
* Integrate with external payroll systems
* Log all actions for audit purposes

---

## 2. System Overview

The system consists of:

* Frontend (HR Interface)
* Backend API Layer
* Database
* Integration with Payroll System

---

## 3. System Architecture

### 3.1 High-Level Architecture

* Client → Frontend UI
* Frontend → REST API
* API → Database
* API → Payroll System

---

## 4. Data Model

### 4.1 Employee Table

| Field      | Type   | Description        |
| ---------- | ------ | ------------------ |
| id         | UUID   | Unique employee ID |
| name       | String | Employee name      |
| department | String | Department         |

---

### 4.2 Salary Table

| Field          | Type      | Description           |
| -------------- | --------- | --------------------- |
| id             | UUID      | Salary record ID      |
| employee_id    | UUID      | Reference to employee |
| salary_amount  | Decimal   | Salary amount         |
| currency       | String    | Currency type         |
| effective_date | Date      | Start date            |
| created_at     | Timestamp | Created time          |

---

### 4.3 Salary History Table

| Field      | Type      | Description     |
| ---------- | --------- | --------------- |
| id         | UUID      | History ID      |
| salary_id  | UUID      | Reference       |
| old_value  | Decimal   | Previous salary |
| new_value  | Decimal   | Updated salary  |
| changed_by | String    | User            |
| changed_at | Timestamp | Time            |

---

## 5. API Requirements

### 5.1 Create Salary

**POST /salaries**

Request:

```json
{
  "employee_id": "uuid",
  "salary_amount": 5000,
  "currency": "USD"
}
```

Response:

```json
{
  "status": "success",
  "salary_id": "uuid"
}
```

---

### 5.2 Update Salary

**PUT /salaries/{id}**

---

### 5.3 Get Salary History

**GET /salaries/{id}/history**

---

## 6. Business Rules

* Salary updates must create a history record
* Only HR role can create/update salaries
* Salary cannot be negative
* Effective date cannot be in the past

---

## 7. Security Requirements

* Role-based authentication (RBAC)
* Secure API access (JWT)
* Data encryption for sensitive data

---

## 8. Performance Requirements

* API response time < 2 seconds
* System must support 10,000+ employees

---

## 9. Error Handling

* Invalid input → 400 Bad Request
* Unauthorized → 401
* Server error → 500

---

## 10. Integration Requirements

* System must send salary data to payroll system via API
* Data format must be JSON

---

## 11. Audit & Logging

* Log all create/update actions
* Store user and timestamp
* Logs must be immutable
