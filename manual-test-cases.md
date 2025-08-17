# Manual Test Cases - Flight Booking System

> **Note:**  
> The Flight Booking System was developed as a **capstone project** for **academic and training purposes only**.  
> It is **not an actual flight booking service**.  
> The system supports **local flights within the Philippines only**, and integrates with third-party APIs for **flight schedules**.  
> International routes are **not included**.
> Payment services are **simulated**.

---

## 1. Flight Search
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| FS-01   | Search with valid input | User on search page | Enter valid origin, destination, and date (local flight) | System displays available flights from schedule API |
| FS-02   | Search with invalid date | User on search page | Enter a past date | Error message displayed (invalid date) |
| FS-03   | Search with missing input | User on search page | Leave origin or destination blank | System prompts user to complete input |
| FS-04   | Search for unavailable route | User on search page | Enter two cities without any available flights | System shows “No flights available” |

---

## 2. Flight Booking
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| FB-01   | Book flight with valid data | User has selected a valid flight | Enter passenger details and confirm booking | Booking confirmation displayed with ticket ID |
| FB-02   | Book flight with missing passenger details | User has selected a valid flight | Leave mandatory fields empty | System prompts user to fill in required fields |
| FB-03   | Attempt to book full flight | User selects flight marked as full | Try to confirm booking | System displays “Flight fully booked” message |

---

## 3. Ticket Generation
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| TG-01   | Generate ticket after booking | Booking successfully completed | Confirm booking | System generates unique ticket with flight + passenger details |
| TG-02   | View ticket details | Ticket already generated | Open “My Tickets” page | System displays passenger and flight information correctly |

---

## 4. Cancellation & Refund
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| CR-01   | Cancel valid booking | User has a confirmed ticket | Select booking → Cancel | System cancels booking and marks ticket as void |
| CR-02   | Cancel already-cancelled booking | User has a cancelled ticket | Try to cancel again | System displays “Booking already cancelled” |
| CR-03   | Refund process check (training simulation only) | User has a cancelled booking | Request refund | System confirms refund request (simulation only, no real payment) |

---

## 5. API Integration (Flight Schedules)
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| API-01  | Retrieve flight schedule successfully | API is available | Search for valid flight | System fetches and displays updated flight schedule |
| API-02  | API unavailable | API service is down | Search for flight | System displays error: “Unable to fetch flight schedule” |
| API-03  | Invalid API response | API returns corrupted/missing fields | Search for flight | System handles gracefully (default error message shown) |
| API-04  | No schedule available for route | API returns empty result | Search for non-existing route | System shows “No flights available” |

---

## 6. Negative & Edge Cases
| Test ID | Test Case Description | Precondition | Steps | Expected Result |
|---------|----------------------|--------------|-------|-----------------|
| NE-01   | Enter numbers in name field | User on booking form | Enter digits in passenger name | System rejects invalid input |
| NE-02   | Extremely long passenger name | User on booking form | Enter >100 characters in name | System shows validation error |
| NE-03   | Search with same origin and destination | User on search page | Enter same city for both fields | System rejects input with error message |

---
