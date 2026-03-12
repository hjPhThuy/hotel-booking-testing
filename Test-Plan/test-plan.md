# Test Plan – Hotel Booking Web Application

## 1. Introduction
This document describes the testing plan for the Hotel Booking Web Application.

The goal of testing is to verify that the system works correctly and allows users to search, book, and manage hotel reservations without errors.

---

## 2. Objectives

The objectives of testing include:

- Verify that the hotel booking system functions correctly
- Ensure users can search and book rooms successfully
- Identify defects in the system
- Validate user inputs and booking data

---

## 3. Scope of Testing

### In Scope

**Authentication**
- User registration
- User login
- User logout

**Room Features**
- View room list
- View room details
- Search available rooms

**Booking**
- Book a room
- Cancel booking
- View booking history

### API Testing
API endpoints will be tested using Postman.

---

## 4. Test Strategy

### Functional Testing
Verify that all features work according to requirements.

### Validation Testing
Check input validation such as:

- Email format
- Required fields
- Date validation

### UI Testing
Verify that UI elements such as buttons, forms, and messages display correctly.

### API Testing
Test API responses and data returned from the server.

---

## 5. Test Environment

| Item          | Description 

| Application   | Hotel Booking Web Application 
| Browser       | Google Chrome          
| OS            | Windows  
| API Tool      | Postman 

---

## 6. Test Deliverables

The following documents will be created:

- Test Plan
- Test Scenarios
- Test Cases
- Bug Reports
- API Testing Collection
