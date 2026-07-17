# Test Scenarios & Test Cases

## Employee Salary Management System

---

## 🧩 Test Scenario 1: Create Salary Record

### TC-01: Valid Salary Creation

**Precondition:** Employee exists

**Steps:**

1. Navigate to salary creation screen
2. Enter employee ID
3. Enter valid salary amount
4. Select currency
5. Click save

**Expected Result:**

* Salary record is created successfully
* Record is stored in database

---

### TC-02: Invalid Salary Amount

**Steps:**

1. Enter salary as negative value
2. Click save

**Expected Result:**

* System shows validation error
* Salary is not saved

---

## 🧩 Test Scenario 2: Update Salary

### TC-03: Update Salary Successfully

**Precondition:** Salary record exists

**Steps:**

1. Select existing salary
2. Update salary amount
3. Save changes

**Expected Result:**

* Salary is updated
* Previous value is stored in history

---

### TC-04: Check Salary History

**Steps:**

1. Open salary history screen

**Expected Result:**

* Previous salary values are displayed
* Includes timestamp and user

---

## 🔐 Test Scenario 3: Authorization

### TC-05: Unauthorized Access

**Steps:**

1. Login as non-HR user
2. Try to create salary

**Expected Result:**

* Access is denied
* Error message displayed

---

## 🔄 Test Scenario 4: API Integration

### TC-06: Send Salary to Payroll

**Steps:**

1. Trigger payroll integration

**Expected Result:**

* Salary data is sent successfully
* API returns success response

---

## ⚠️ Edge Cases

### TC-07: Missing Employee ID

**Expected Result:**

* System throws validation error

### TC-08: Large Salary Value

**Expected Result:**

* System handles large numbers correctly
