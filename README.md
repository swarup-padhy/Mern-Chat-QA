<div align="center">

# Real-Time Chat Application — Manual Testing

### *Black Box QA Audit — Functional · UI · Resilience Testing*

<br/>

![Testing Type](https://img.shields.io/badge/Testing-Manual%20Black%20Box-4A90D9?style=for-the-badge&logo=testcafe&logoColor=white)
![Scope](https://img.shields.io/badge/Scope-Functional%20%7C%20UI%20%7C%20Resilience-8E44AD?style=for-the-badge&logoColor=white)
![Status](https://img.shields.io/badge/Status-RC1%20Complete-2ECC71?style=for-the-badge&logo=checkmarx&logoColor=white)

<br/>

**QA Engineer:** Swarup Padhy &nbsp;|&nbsp; **Application Under Test:** [Fullstack Chat App](https://github.com/burakorkmez/fullstack-chat-app) by [Burak Orkmez](https://github.com/burakorkmez)

</div>

---

## Project Overview

This repository contains all **Manual Testing artifacts** for a full-stack Real-Time Chat Application. The objective is to demonstrate a structured QA process — covering test planning, scenario design, test case execution, and defect reporting across functional, UI, and resilience dimensions.

**Testing Scope:** Black Box Testing · Functional Testing · UI Validation · Resilience & Edge Cases

---

## QA Artifacts

| Artifact | Description |
|---|---|
| [TEST_PLAN.md](./TEST_PLAN.md) | High-level strategy, scope, environment, and pass/fail criteria |
| [01_SCENARIOS.md](./01_SCENARIOS.md) | Functional breakdown of user flows and test scenarios |
| [02_TEST_CASES.md](./02_TEST_CASES.md) | Detailed test steps with execution status (Pass/Fail) |
| [03_BUG_REPORTS.md](./03_BUG_REPORTS.md) | Central dashboard for tracking all identified defects |
| [Bug-Reports/](./Bug-Reports/) | Individual detailed bug reports for each reported issue |

---

## Testing Highlights

| Area | Detail |
|---|---|
| **Methodology** | Manual Functional Testing |
| **Key Modules** | Authentication · Real-Time Messaging · Profile Management |
| **Tools** | Chrome DevTools (Network Throttling, Console Logs) · Multiple Browser Sessions |
| **Test Cycle** | Release Candidate 1 — Testing Complete |

---

## How to Run Locally (For Verification)

To verify reported bugs or execute test cases yourself:

### Clone the Application
```bash
git clone https://github.com/burakorkmez/fullstack-chat-app.git
cd fullstack-chat-app
```

### Start the Backend
```bash
npm run start   # Backend → http://localhost:5000
```

### Start the Frontend
```bash
cd frontend
npm run dev     # Frontend → http://localhost:5173
```

---

<div align="center">

### Summary

This audit demonstrates practical application of **manual QA processes** — from structured test planning through to defect lifecycle management across a real-time, full-stack application.

<br/>

*Tested with 🔬 Chrome DevTools · 🖥️ Multi-Session Browser Testing · 📋 Manual Execution*

</div>
