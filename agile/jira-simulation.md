### 🟦 STORY: US-01 Create Salary Record

**Type:** Story
**Epic Link:** EPIC-1 Salary Management

**Description:**
As an HR Specialist, I want to create a salary record so that employee salary data can be stored.

---

**Acceptance Criteria:**

1. Salary can be created with employee ID
2. Salary must be greater than 0
3. Currency must be selected
4. Data is saved successfully

---

**Tasks:**

* Create API endpoint (POST /salaries)
* Design database insert logic
* Build UI form for HR
* Add validation

---

**Story Points:** 5
**Priority:** High
**Status:** To Do




### 🟦 STORY: US-02 Update Salary

**Type:** Story
**Epic Link:** EPIC-1 Salary Management

**Description:**
As an HR Specialist, I want to update salary so that changes are reflected in the system.

---

**Acceptance Criteria:**

1. Salary can be updated
2. Previous value stored in history
3. Timestamp and user recorded

---

**Tasks:**

* Update API endpoint (PUT /salaries)
* Implement history logic
* Update UI
* Add validation

---

**Story Points:** 5
**Priority:** High
**Status:** To Do




### 🟥 BUG: Salary accepts negative value

**Type:** Bug

**Description:**
System allows saving salary with negative value.

---

**Steps to Reproduce:**

1. Go to salary creation
2. Enter -5000
3. Click save

---

**Expected Result:**
System should reject negative values

**Actual Result:**
Salary is saved successfully

---

**Priority:** High
**Status:** Open
