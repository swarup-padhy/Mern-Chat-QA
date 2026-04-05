# Chat Application — Manual Testing Project

> A structured manual testing engagement covering core functional, security, and real-time requirements of a MERN chat application.

---

![Test Cases](https://img.shields.io/badge/Test%20Cases-29-brightgreen?style=flat-square)
![Passed](https://img.shields.io/badge/Passed-25-success?style=flat-square)
![Failed](https://img.shields.io/badge/Failed-4-critical?style=flat-square)
![Defects](https://img.shields.io/badge/Defects-4%20Open-red?style=flat-square)
![Coverage](https://img.shields.io/badge/Requirement%20Coverage-100%25-blue?style=flat-square)
![Status](https://img.shields.io/badge/Cycle%20Status-Complete-blueviolet?style=flat-square)

---

## Project Overview

| Field | Detail |
| :--- | :--- |
| **Application** | Fullstack Chat App (MERN Stack + Socket.io) |
| **Source Code** | [github.com/burakorkmez/fullstack-chat-app](https://github.com/burakorkmez/fullstack-chat-app) |
| **Testing Type** | Manual — Functional, API, Security, Real-Time |
| **Tester** | Swarup Padhy |
| **Environment** | Windows 11 · Chrome · Node.js (Local) · MongoDB |
| **Tools Used** | Postman · Chrome DevTools · MongoDB Compass · Firefox |

---

## What Was Tested

| Area | Description |
| :--- | :--- |
| 🔐 **Authentication** | Signup, Login, Logout, JWT cookie lifecycle, session restore, route protection |
| 💬 **Messaging** | Text and image sending, chat history loading, message consistency |
| ⚡ **Real-Time (Socket.io)** | Live message delivery, online/offline presence, socket lifecycle on logout |
| 🛡️ **Security** | XSS injection, JWT token reuse after logout, duplicate email bypass |
| 🔌 **API Validation** | Status codes, auth middleware enforcement, malformed request handling |
| 🪟 **Session Handling** | Multi-tab sync, session persistence after full browser restart |

---

## Defects Discovered

| Bug ID | Title | Severity | Requirement | Status |
| :--- | :--- | :--- | :--- | :--- |
| [BUG-001](04-defects/defect-log.md) | Case-variant emails bypass duplicate account check | 🔴 High | REQ-AUTH-07 | Open |
| [BUG-002](04-defects/defect-log.md) | JWT token not invalidated on server after logout | 🔴 Critical | REQ-AUTH-05 | Open |
| [BUG-003](04-defects/defect-log.md) | Image messages fail to send in chat | 🔴 High | REQ-MSG-03 | Open |
| [BUG-004](04-defects/defect-log.md) | WebSocket stays open after logout (Zombie Connection) | 🔴 High | REQ-TECH-02 | Open |

---

## Test Execution Summary

| Status | Count | Coverage |
| :--- | :---: | :--- |
| ✅ Passed | 25 | ████████████████████░░░ 86% |
| ❌ Failed | 4 | ██░░░░░░░░░░░░░░░░░░░░░ 14% |
| **Total** | **29** | **100% Executed** |

---

## Repository Structure

```
chat-app-manual-testing/
│
├── README.md
│
├── 📁 01-requirements/
│   └── requirements.md          ← What the system must do (21 requirements)
│
├── 📁 02-test-plan/
│   └── test-plan.md             ← Strategy, scope, risks, environment
│
├── 📁 03-test-design/
│   ├── test-scenarios.md        ← 26 high-level test scenarios
│   ├── test-cases.md            ← 29 detailed test cases with execution status
│   └── api-inventory.md         ← All 8 API endpoints mapped to test cases
│
├── 📁 04-defects/
│   └── defect-log.md            ← All 4 defects with steps, evidence, fix notes
│
├── 📁 05-rtm/
│   └── rtm.md                   ← Full REQ → TS → TC → BUG traceability map
│
└── 📁 evidence/
    ├── BUG-001/                  ← MongoDB screenshot: duplicate email records
    ├── BUG-002/                  ← Session recording: JWT reuse after logout
    ├── BUG-003/                  ← Screenshot: image send failure in chat
    └── BUG-004/                  ← Before/After screenshots: zombie WebSocket
```

---

## Traceability Flow

Every test case traces back to a documented requirement. No test exists without a reason. No requirement goes untested.

```
REQ  ──►  TS  ──►  TC  ──►  BUG
(What)  (Behavior) (Steps) (Finding)
```

**Example chain:**
```
REQ-AUTH-07  ──►  TS-AUTH-02  ──►  TC-AUTH-04  ──►  BUG-001
Duplicate email    Registration     Case-variant      Two accounts
must be rejected   must fail        email test        created in DB
```

→ Full matrix in [`05-rtm/rtm.md`](05-rtm/rtm.md)

---

## API Coverage

| Endpoint | Method | Auth | Covered By |
| :--- | :--- | :--- | :--- |
| `/auth/signup` | POST | No | TC-AUTH-01, 02, 03, 04 |
| `/auth/login` | POST | No | TC-AUTH-05, 07 |
| `/auth/logout` | POST | No | TC-AUTH-09 |
| `/auth/check` | GET | ✅ Yes | TC-AUTH-08, TC-SESSION-11 |
| `/auth/update-profile` | PUT | ✅ Yes | TC-PRF-01, 02 |
| `/messages/users` | GET | ✅ Yes | TC-MSG-01, TC-API-10 |
| `/messages/:id` | GET | ✅ Yes | TC-MSG-02 |
| `/messages/send/:id` | POST | ✅ Yes | TC-MSG-03, 04, 05, 06, TC-API-12 |

---

## Key Testing Techniques Used

- **Boundary Value Analysis** — Password length (5 chars fail · 6 chars pass)
- **Negative Testing** — Wrong passwords, malformed requests, unauthorized API calls
- **Exploratory Testing** — Discovered BUG-002 (JWT reuse) and BUG-004 (zombie socket) without predefined scripts
- **Cookie Inspection** — DevTools used to verify `HttpOnly`, `Secure`, `SameSite=Strict` flags
- **WebSocket Monitoring** — Network tab used to observe real-time socket lifecycle
- **Database Verification** — MongoDB Compass used to confirm password hashing and duplicate records
- **XSS Injection** — Script payloads tested in message input and signup name fields
- **Multi-Session Testing** — Chrome + Edge used simultaneously for real-time presence verification
