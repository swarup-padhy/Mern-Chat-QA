# Real-Time Chat Application - QA Documentation

## Project Overview
This project is a full-stack real-time chat application built using the MERN stack (MongoDB, Express, React, Node.js) and Socket.io for real-time capabilities.

### Key Features
- **Authentication**: User Signup, Login, and Logout.
- **Real-Time Messaging**: Instant message delivery and updates.
- **User Presence**: See online/offline status of users.
- **Theming**: Switch between different light/dark themes (DaisyUI).
- **Profile Management**: Update user profile information.

## Tech Stack
- **Frontend**: React, Vite, TailwindCSS, DaisyUI, Zustand (State Management), Axios.
- **Backend**: Node.js, Express, Socket.io, Mongoose (MongoDB).
- **Environment**: Node.js v20+ recommended.

## Setup Instructions

### Prerequisites
- Node.js installed.
- MongoDB instance (local or Atlas URI).
- `.env` file in the project root.

### Installation & Running
1.  **Install Dependencies**:
    ```bash
    npm install --prefix backend
    npm install --prefix frontend
    ```

2.  **Start Backend**:
    ```bash
    npm start
    # Runs on port 5001 by default
    ```

3.  **Start Frontend**:
    ```bash
    cd frontend
    npm run dev
    # Runs on http://localhost:5173
    ```

## QA Folder Structure
- `README.md`: This file.
- `TEST_PLAN.md`: Overall testing strategy.
- `01_SCENARIOS.md`: High-level test scenarios.
- `02_TEST_CASES.md`: Detailed manual test cases (User Managed).
- `03_BUG_REPORTS.md`: Defect tracking (User Managed).
