#  Booking System – QA Testing Project

##  Overview

This project demonstrates my QA testing skills through testing a **Booking System API**.
The testing covers multiple modules including authentication, booking, hotels, rooms, users, and reviews.

---

##  Objectives

* Perform end-to-end API testing
* Identify bugs and validation issues
* Verify system behavior and data consistency
* Practice real-world QA workflow

---

##  Tools & Technologies

* **Postman** – API testing
* **GitHub** – Project management
* **Markdown** – Documentation

---

##  Project Structure

```
.
├── Test-Cases/
├── Test-Plan/
├── bug-reports/
├── api-testing/
│   ├── postman
│   ├── api-test-doc.md
├── README.md
```

---

##  Testing Scope

### Modules Tested

* 🔑 Authentication
* 👤 Users
* 🏨 Hotels
* 🛏️ Rooms
* 📅 Bookings
* ⭐ Reviews

---

## Testing Types

* Functional Testing
* Validation Testing
* Security Testing
* Edge Case Testing

---

##  Key Findings

###  Critical / High Bugs

* Booking allows past date
* Booking allows negative guests
* Room allows negative price

###  Medium Bugs

* Invalid phone format accepted
* Missing images still creates room
* API returns incorrect HTTP status codes

###  System Issues

* Debug API does not return booking data
* Inconsistent error messages

---

##  API Testing

All API test cases are executed using Postman.

See details in:

```
api-testing/
```

---

##  Key Learnings

* Learned how to test APIs without documentation by inspecting network requests
* Understood dependencies between modules (Booking → Review)
* Identified validation and business logic issues
* Improved bug reporting and test design skills

---

##  Conclusion

The system contains several validation and design issues that should be fixed before production release.

This project demonstrates my ability to:

* Design test scenarios
* Execute API testing
* Identify real-world bugs
* Document findings clearly

---

##  Author

**Lâm Nguyễn Phương Thùy**
QA / Tester

---
