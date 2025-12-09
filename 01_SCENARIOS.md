# 01 - Test Scenarios

## 1. Authentication Module

### TS-AUTH-01: User Signup
- **TS-AUTH-01-01**: Verify successful signup with all valid fields (Name, Email, Password).
- **TS-AUTH-01-02**: Verify signup fails with empty "Full Name".
- **TS-AUTH-01-03**: Verify signup fails with empty "Email".
- **TS-AUTH-01-04**: Verify signup fails with invalid email format (e.g., missing @).
- **TS-AUTH-01-05**: Verify signup fails with empty "Password".
- **TS-AUTH-01-06**: Verify signup fails with password less than 6 characters (if applicable).
- **TS-AUTH-01-07**: Verify signup fails if email is already registered.
- **TS-AUTH-01-08**: Verify "Sign user up" button enters loading state/disabled during request.

### TS-AUTH-02: User Login
- **TS-AUTH-02-01**: Verify successful login with valid email and password.
- **TS-AUTH-02-02**: Verify login fails with incorrect password.
- **TS-AUTH-02-03**: Verify login fails with non-existent email.
- **TS-AUTH-02-04**: Verify login fails with empty fields.
- **TS-AUTH-02-05**: Verify navigation to Signup page from "Create account" link.

### TS-AUTH-03: User Logout
- **TS-AUTH-03-01**: Verify logout functionality clears user session.
- **TS-AUTH-03-02**: Verify redirection to Login page after logout.

## 2. Real-Time Chat Module

### TS-CHAT-01: User Selection & Sidebar
- **TS-CHAT-01-01**: Verify sidebar lists online users correctly.
- **TS-CHAT-01-02**: Verify selecting a user opens the correct chat window.
- **TS-CHAT-01-03**: Verify "No conversation selected" placeholder is shown initially.
- **TS-CHAT-01-04**: Verify sidebar loading skeleton appears while fetching users.

### TS-CHAT-02: Message Sending
- **TS-CHAT-02-01**: Verify sending a text message updates the UI immediately.
- **TS-CHAT-02-02**: Verify sending an image message (upload/attachment).
- **TS-CHAT-02-03**: Verify sending empty message is prevented.
- **TS-CHAT-02-04**: Verify input field clears after sending.

### TS-CHAT-03: Message Reception
- **TS-CHAT-03-01**: Verify receiving a text message in real-time.
- **TS-CHAT-03-02**: Verify receiving an image message in real-time.
- **TS-CHAT-03-03**: Verify chat auto-scrolls to the bottom on new message.

### TS-CHAT-04: Chat History
- **TS-CHAT-04-01**: Verify previous messages are loaded when opening a chat.
- **TS-CHAT-04-02**: Verify format of timestamps on messages.

## 3. User & Settings Module

### TS-USER-01: Profile Management
- **TS-USER-01-01**: Verify Profile page displays correct user information.
- **TS-USER-01-02**: Verify uploading a new profile picture.
- **TS-USER-01-03**: Verify updated profile picture reflects in the header/sidebar.
- **TS-USER-01-04**: Verify error handling for invalid image file types/sizes.

### TS-SET-01: Theme Switching
- **TS-SET-01-01**: Verify switching to "Dark" theme.
- **TS-SET-01-02**: Verify switching to "Light" theme.
- **TS-SET-01-03**: Verify switching to "Retro" theme (or other variants).
- **TS-SET-01-04**: Verify selected theme persists after browser refresh.

## 4. Network & Resilience

### TS-NET-01: Connectivity
- **TS-NET-01-01**: Verify behavior when backend is unconnected (Network Error toast).
- **TS-NET-01-02**: Verify system recovery when backend comes back online.
