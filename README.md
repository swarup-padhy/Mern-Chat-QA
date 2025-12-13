# Real-Time Chat Application - Manual Testing Portfolio

## 1. Project Overview
This repository contains the **Manual Testing artifacts** for a full-stack Real-Time Chat Application. The primary objective is to demonstrate industry-standard QA processes, including test planning, scenario design, test case execution, and bug reporting.

### 📌 Project Context & Credits
* **Application Under Test**: [Fullstack Chat App](https://github.com/burakorkmez/fullstack-chat-app)
* **Original Developer**: [Burak Orkmez](https://github.com/burakorkmez)
* **QA Engineer**: [Your Name/Role] - DevOps & QA Lead
* **Testing Scope**: Black Box Testing (Functional, UI, and Resilience)

> **Note**: This project is for **educational and portfolio purposes**. The documentation below reflects a simulated professional QA environment auditing the application for release readiness.

---

## 2. QA Artifacts
This folder is structured to mirror a real-world testing cycle:

| File / Folder | Description |
|--------------|-------------|
| [**TEST_PLAN.md**](./TEST_PLAN.md) | High-level strategy, scope, environment, and pass/fail criteria. |
| [**01_SCENARIOS.md**](./01_SCENARIOS.md) | Functional breakdown of user flows and test scenarios. |
| [**02_TEST_CASES.md**](./02_TEST_CASES.md) | Detailed test steps with execution status (Pass/Fail). |
| [**03_BUG_REPORTS.md**](./03_BUG_REPORTS.md) | Central dashboard for tracking identified defects. |
| [**Bug-Reports/**](./Bug-Reports/) | Individual, detailed bug reports for reported issues. |

## 3. Testing Highlights
- **Methodology**: Manual Functional Testing.
- **Key Modules Tested**: Authentication, Real-Time Messaging, Profile Management.
- **Tools**: Chrome DevTools (Network Throttling, Console Logs), Multiple Browser Sessions.
- **Status**: Release Candidate 1 Testing Complete.

---

## 4. How to Run Locally (For Verification)
To verify the reported bugs or execute test cases yourself:

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/burakorkmez/fullstack-chat-app.git
    cd fullstack-chat-app
    ```

2.  **Start Backend**:
    ```bash
    npm run start
    ```

3.  **Start Frontend**:
    ```bash
    cd frontend
    npm run dev
    ```
