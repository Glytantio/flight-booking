# Test Plan - Flight Booking System

## 1. Introduction
This document defines the testing scope, objectives, and approach for the **Flight Booking System**.  
The system was developed as part of an **academic capstone project** and is intended for **training purposes only**.  

It is **not a real-world flight booking service**.  
The system is limited to **local flights in the Philippines**, retrieves schedules through **third-party APIs**, and includes **simulated payment services** to make the experience more realistic.

---

## 2. Scope

### In-Scope
- Local flights within the Philippines
- Flight search, booking, ticket generation, and cancellation
- Retrieval of **flight schedules from third-party APIs**
- **Simulated payment services** (mock card details, training-only)

### Out-of-Scope
- International flights
- Real-world payment processing or gateway integration
- Airline backend systems outside the training environment

---

## 3. Objectives
- Verify that users can **search, book, and manage local flights**.
- Ensure accurate retrieval of flight schedules via APIs.
- Validate correct handling of simulated payments (success, failure, retry, cancel).
- Confirm cancellation and refund behavior.
- Test negative and edge cases to ensure robustness.

---

## 4. Test Strategy
- **Manual Testing**: Primary method using Markdown-based test cases.
- **Functional Testing**: Verify that each feature behaves as expected.
- **Negative Testing**: Validate system response to invalid or unexpected inputs.
- **Regression Testing**: Ensure updates don’t break existing functionality.
- **API Testing**: Verify schedule data retrieval and error handling.
- **Payment Simulation Testing**: Validate transaction scenarios using mock data.

---

## 5. Test Environment
- **Browsers**: Chrome, Firefox  
- **Operating Systems**: Windows 10, Linux (Ubuntu)  
- **Data Source**: Third-party APIs (flight schedules only, local flights)  
- **Payment Simulation**: Mock payment services (training-only, no real transactions)  

---

## 6. Deliverables
- `manual-test-cases.md` → Detailed test cases  
- Test results (to be updated during execution)  
- Supporting diagrams in `/docs`  

---

## 7. Risks & Mitigation
- **API downtime or unavailability** → Use mock test data as fallback.  
- **Incomplete data for certain local routes** → Validate system behavior with missing schedules.  
- **Payment simulation issues** → Ensure clear messages are displayed; no real financial risk.  
- **Scope confusion (academic vs real-world)** → Explicit disclaimers in all documentation.  

---

## 8. Approval
This test plan is prepared for **academic and training use only**, as part of the Flight Booking System capstone project.
