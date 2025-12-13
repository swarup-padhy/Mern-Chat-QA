# Test Plan: Real-Time Chat Application

## 1. Introduction
This document outlines the testing strategy for the Release Candidate 1 (RC1) of the Real-Time Chat Application. The goal is to ensure core functionality, data integrity, and user experience meet quality standards before deployment.

## 2. Scope
### 2.1 In-Scope
-   **Authentication**: Signup, Login, Logout behavior and validation.
-   **Core Messaging**: Real-time sending/receiving of text and images.
-   **User Interface**: Sidebar updates, Profile management, and Theme switching.
-   **Resilience**: Application behavior during network interruptions.

### 2.2 Out-Scope
-   Backend API load testing.
-   Security penetration testing.
-   Code-level unit testing (responsibility of Development Team).

## 3. Test Strategy
### 3.1 Testing Levels
-   **Smoke Testing**: Verify critical paths (Login → Send Message) are unblocked.
-   **Functional Testing**: Validate all requirements against expected behavior.
-   **Exploratory Testing**: Ad-hoc testing to discover edge cases and usability issues.

### 3.2 Tools & Environment
-   **OS**: Windows 11
-   **Browsers**: Google Chrome (Primary), Edge (Secondary).
-   **Network Simulation**: Chrome DevTools (Slow 3G, Offline).

## 4. Defect Managment
-   **Reporting**: All bugs are logged in the `Bug-Reports` directory.
-   **Severity Scale**:
    -   **Critical**: Blocker (e.g., App crash, Data loss).
    -   **Major**: Core feature broken, no workaround.
    -   **Minor**: UI/Cosmetic issue or workaround available.
    -   **Low**: Suggestion / trivial issue.

## 5. Deliverables
-   Test Plan (This document)
-   Test Scenarios & Cases
-   Defect Reports
-   Final Test Summary
