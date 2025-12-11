## Real-Time Chat Application - QA Notes

**Engineer**: DevOps & QA Lead
**Date**: December 2024

### Overview
This is a standard MERN stack chat app. It's clean, functional, and uses Socket.io for the heavy lifting. I've run through the full test suite and it's holding up well.

### Quick Start (Dev Mode)
Don't overcomplicate it. Just get the backend and frontend running.

1. **Backend**:
   ```bash
   npm start # Runs on port 5001
   ```
2. **Frontend**:
   ```bash
   cd frontend && npm run dev # Runs on localhost:5173
   ```

### QA Artifacts in this Folder
- **`TEST_PLAN.md`**: My strategy. Simple and execution-focused.
- **`01_SCENARIOS.md`**: The user flows we care about.
- **`02_TEST_CASES.md`**: The nitty-gritty checks. **(Executed & Passed)**
- **`03_BUG_REPORTS.md`**: Current defect list. (Clean as of RC1)

---
*Keep it simple, keep it shipping.*
