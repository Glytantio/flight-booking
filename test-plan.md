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
- Confirm that cancellation and refund logic works within defined limits
