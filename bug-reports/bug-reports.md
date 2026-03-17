#  Bug Report – Booking System Testing

##  Overview

* **Project:** Booking System
* **Testing Type:** Manual Testing
* **Total Test Cases:** 40
* **Total Bugs Found:** 5
* **Environment:**

  * OS: Windows 10
  * Browser: Chrome 145

---

##  Bug Summary

| Bug ID     | Title                                                    | Severity | Priority | Status |
| ---------- | -------------------------------------------------------- | -------- | -------- | ------ |
| BOOK-001   | Booking created with past date                           | High     | High     | Open   |
| BOOK-002   | Booking allows exceeding max guests                      | Medium   | High     | Open   |
| BOOK-003   | Unauthorized access to My Bookings page                  | High     | High     | Open   |
| OWN-001    | Room created with negative price & duplicate submissions | Critical | High     | Open   |
| REVIEW-001 | System requires comment when it should be optional       | Low      | Medium   | Open   |

---

##  BUG-001: Booking with Past Date

**Severity:** High
**Priority:** High
**Module:** Booking

### Precondition

* User is logged in

### Steps to Reproduce

1. Navigate to Booking page
2. Select a past date
3. Click "Book"

### Actual Result

* Booking is created successfully
* Confirmation message is displayed

### Expected Result

* System should reject booking with past date
* Validation error message should be shown

---

##  BUG-002: Exceeding Maximum Guests

**Severity:** Medium
**Priority:** High
**Module:** Booking

### Precondition

* User is logged in

### Steps to Reproduce

1. Select number of guests greater than allowed maximum
2. Click "Book"

### Actual Result

* Booking is created successfully

### Expected Result

* Validation error message should be displayed
* Booking should not be created

---

##  BUG-003: Unauthorized Access to My Bookings

**Severity:** High (Security Issue) 
**Priority:** High
**Module:** Booking

### Precondition

* User is not logged in

### Steps to Reproduce

1. Open browser
2. Enter URL `/my-bookings` directly

### Actual Result

* My Bookings page is loaded
* Toast message: "Not authorized, token failed" appears

### Expected Result

* User should be redirected to login page
* Access should be blocked completely

---

##  BUG-004: Negative Price & Duplicate Room Creation

**Severity:** Critical 
**Priority:** High
**Module:** Owner Rooms

### Precondition

* Admin is logged in

### Steps to Reproduce

1. Enter a negative price value
2. Click "Save" multiple times

### Actual Result

* No validation message displayed
* Room is created with negative price
* Multiple rooms are created due to repeated clicks

### Expected Result

* System should validate that price must be greater than 0
* Only one submission should be processed
* Submit button should be disabled after first click

---

##  BUG-005: Review Requires Comment Incorrectly

**Severity:** Low
**Priority:** Medium
**Module:** Review

### Precondition

* User is logged in

### Steps to Reproduce

1. Select rating only (without comment)
2. Click "Submit"

### Actual Result

* System prevents submission
* Requires user to enter comment

### Expected Result

* Review should be submitted successfully if comment is optional

---

## 📎 Notes

* Multiple issues related to **input validation** and **business logic enforcement** were identified
* One **security vulnerability** detected (unauthorized access)
* One **data integrity issue** detected (duplicate submissions)
* Suggested improvements:

  * Disable submit button after first click
  * Implement proper validation for all inputs
  * Enforce authentication checks on protected routes

---
