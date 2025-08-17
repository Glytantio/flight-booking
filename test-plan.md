# Test Plan - Flight Booking System

## 1. Introduction
This document defines the testing scope, objectives, and approach for the **Flight Booking System**.  
The system was developed as part of an **academic capstone project** and is intended for **training purposes only**.  

It is **not a real-world flight booking service**.  
The system is limited to **local flights in the Philippines**, and schedules are retrieved through **third-party APIs** for realism.

---

## 2. Scope

### In-Scope
- Local flights within the Philippines
- Flight search, booking, ticket generation, and cancellation
- Retrieval of **flight schedules from third-party APIs**

### Out-of-Scope
- International flights
- Payment processing or payment simulation
- Airline backend systems outside the training environment

---

## 3. Objectives
- Verify that users can **search, book, and manage local flights**.
- Ensure accurate retrieval of flight schedules via APIs.
- Validate correct error handling for invalid inputs and unavailable flights.
- Confirm that cancellation and refund logic works within defined limits.

---

## 4. Test Strategy
- **Manual Testing**: Primary method using test cases in Markdown.
- **Functional Testing**: Verify that each feature behaves as expected.
- **Negative Testing**: Validate how the system handles invalid or unexpected input.
- **Regression Testing**: Ensure that updates don’t break existing functionality.
- **API Testing**: Check data consistency and error handling from schedule APIs.

---

## 5. Test Environment
- **Browsers**: Chrome, Firefox  
- **Operating Systems**: Windows 10, Linux (Ubuntu)  
- **Data Source**: Third-party APIs (flight schedules only, local flights)  

---

## 6. Deliverables
- `manual-test-cases.md` → Detailed test cases  
- Test results (to be updated during execution)  
- Supporting diagrams in `/docs`  

---

## 7. Risks & Mitigation
- **API downtime or unavailability** → Add mock test data for fallback.  
- **Incomplete data for certain local routes** → Validate system behavior when schedules are missing.  
- **No payment simulation** → Focus test cases on booking and schedule-related functionality.  

---

## 8. Approval
This test plan is prepared for **academic and training use** only, as part of the Flight Booking System capstone project.
