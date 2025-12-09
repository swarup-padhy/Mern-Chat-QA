# 02 - Manual Test Cases

## Authentication

| TC ID | Scenario ID | Test Steps                                                                                                        | Expected Result                                                                    | Actual Result | Status |
|-------|-------------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------|--------|
| TC-01 | TS-AUTH-01-01 | 1. Navigate to Signup page<br>2. Enter Name: "Test User"<br>3. Enter valid Email<br>4. Enter Password (Minimum 6 characters)<br>5. Click "Create Account" | Account created successfully; Redirected to Home page; Toast: "Account created successfully" |               |        |
| TC-02 | TS-AUTH-01-02 | 1. Navigate to Signup page<br>2. Leave "Full Name" empty<br>3. Enter valid Email & Password<br>4. Click "Create Account" | Signup fails; Error toast: "Full Name is required"                                 |               |        |
| TC-03 | TS-AUTH-01-03 | 1. Navigate to Signup page<br>2. Enter valid Name<br>3. Leave "Email" empty<br>4. Enter Password<br>5. Click "Create Account" | Signup fails; Error toast: "Email is required"                                     |               |        |
| TC-04 | TS-AUTH-01-04 | 1. Navigate to Signup page<br>2. Enter invalid Email (e.g., "testuser")<br>3. Enter other valid fields<br>4. Click "Create Account" | Signup fails; Error message regarding invalid email format                         |               |        |
| TC-05 | TS-AUTH-01-05 | 1. Navigate to Signup page<br>2. Enter valid Name & Email<br>3. Leave "Password" empty<br>4. Click "Create Account" | Signup fails; Error toast: "Password is required"                                  |               |        |
| TC-06 | TS-AUTH-01-06 | 1. Navigate to Signup page<br>2. Enter valid Name & Email<br>3. Enter Password "123"<br>4. Click "Create Account" | Signup fails; Error toast: "Password must be at least 6 characters"                |               |        |
| TC-07 | TS-AUTH-01-07 | 1. Navigate to Signup page<br>2. Enter an existing user's email<br>3. Enter other valid fields<br>4. Click "Create Account" | Signup fails; Error toast: "Email already exists"                                  |               |        |
| TC-08 | TS-AUTH-01-08 | 1. Enter valid data on Signup<br>2. Click "Create Account"<br>3. Observe button state                           | Button changes to "Loading..." or a spinner icon appears during the request        |               |        |
| TC-09 | TS-AUTH-02-01 | 1. Navigate to Login page<br>2. Enter valid Email & Password<br>3. Click "Sign in"                             | Login successful; Redirected to Home page; Toast: "Successfully logged in."        |               |        |
| TC-10 | TS-AUTH-02-02 | 1. Navigate to Login page<br>2. Enter valid Email<br>3. Enter INCORRECT Password<br>4. Click "Sign in"             | Login fails; Error toast: "Invalid credentials"                                    |               |        |
| TC-11 | TS-AUTH-02-03 | 1. Navigate to Login page<br>2. Enter UNREGISTERED Email<br>3. Enter any Password<br>4. Click "Sign in"            | Login fails; Error toast: "Invalid credentials"                                    |               |        |
| TC-12 | TS-AUTH-02-04 | 1. Navigate to Login page<br>2. Leave Email or Password empty<br>3. Click "Sign in"                           | Login fails; Browser validation or toast requesting fields                         |               |        |
| TC-13 | TS-AUTH-02-05 | 1. Navigate to Login page<br>2. Click "Create account" link                                                     | Redirects to Signup page                                                           |               |        |
| TC-14 | TS-AUTH-03-01 | 1. Login to the application<br>2. Click Logout icon in Navbar                                                   | User logged out; Redirected to Login page; Toast: "Successfully logged out."       |               |        |

## Real-Time Chat

| TC ID | Scenario ID | Test Steps                                                                                              | Expected Result                                                          | Actual Result | Status |
|-------|-------------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|--------|
| TC-15 | TS-CHAT-01-01 | 1. Login as User A<br>2. Observe Sidebar                                                              | Sidebar displays a list of users; Online users have a green online indicator |               |        |
| TC-16 | TS-CHAT-01-02 | 1. Login as User A<br>2. Click on "User B" in Sidebar                                                 | Chat window opens for User B; Header displays User B's name              |               |        |
| TC-17 | TS-CHAT-01-03 | 1. Login as User A<br>2. Do not select any user                                                       | "Welcome" / "No conversation selected" placeholder screen displayed        |               |        |
| TC-18 | TS-CHAT-01-04 | 1. Refresh page<br>2. Observe Sidebar immediately                                                       | Loading skeletons displayed while users are being fetched                |               |        |
| TC-19 | TS-CHAT-02-01 | 1. Select User B<br>2. Type "Hello world"<br>3. Press Enter or Send button                             | Message appears in the chat bubble immediately, aligned to the right     |               |        |
| TC-20 | TS-CHAT-02-02 | 1. Select User B<br>2. Click Image attachment icon<br>3. Select valid image<br>4. Click Send            | Image message appears in the chat bubble                                 |               |        |
| TC-21 | TS-CHAT-02-03 | 1. Select User B<br>2. Leave input empty<br>3. Try to click Send                                       | Send button disabled or action has no effect                             |               |        |
| TC-22 | TS-CHAT-02-04 | 1. Type message "Test"<br>2. Send message                                                               | Input field cleared automatically                                        |               |        |
| TC-23 | TS-CHAT-03-01 | 1. Open User A (Browser 1) and User B (Browser 2)<br>2. User A sends "Hi"<br>3. Observe User B screen | "Hi" appears instantly in User B's chat window (left aligned)            |               |        |
| TC-24 | TS-CHAT-03-02 | 1. Open User A & User B<br>2. User A sends Image<br>3. Observe User B screen                           | Image appears instantly in User B's chat window                          |               |        |
| TC-25 | TS-CHAT-03-03 | 1. Fill chat history to be scrollable<br>2. Receive new message                                         | Chat container auto-scrolls to the newest message at the bottom          |               |        |
| TC-26 | TS-CHAT-04-01 | 1. Refresh page<br>2. Click on User B (who has history)                                                 | Previous chat messages load and display correctly                        |               |        |
| TC-27 | TS-CHAT-04-02 | 1. Inspect a message bubble                                                                             | Timestamp displayed (e.g., 10:30 PM)                                     |               |        |

## User & Settings

| TC ID | Scenario ID | Test Steps                                                                                                      | Expected Result                                                           | Actual Result | Status |
|-------|-------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|---------------|--------|
| TC-28 | TS-USER-01-01 | 1. Click Profile icon in Navbar                                                                                 | Profile page opens; Displays correct Name and Email (read-only)           |               |        |
| TC-29 | TS-USER-01-02 | 1. On Profile Page<br>2. Click Camera/Edit icon on Avatar<br>3. Select new image                                | "Profile updated successfully" toast; New avatar displayed                |               |        |
| TC-30 | TS-USER-01-03 | 1. Update avatar in Profile<br>2. Look at Navbar/Sidebar                                                        | New avatar is reflected in Navbar and Sidebar user list                   |               |        |
| TC-31 | TS-USER-01-04 | 1. Try to upload an oversized image (>5MB) OR a non-image file                                                | Error toast handling invalid file                                         |               |        |
| TC-32 | TS-SET-01-01 | 1. Click Settings icon in Navbar<br>2. Select "dark" theme                                                      | UI colors change to dark theme instantly                                  |               |        |
| TC-33 | TS-SET-01-02 | 1. Click Settings icon in Navbar<br>2. Select "light" theme                                                     | UI colors change to light theme instantly                                 |               |        |
| TC-34 | TS-SET-01-03 | 1. Click Settings icon in Navbar<br>2. Select "retro" (or other)                                                | UI colors change to selected theme instantly                              |               |        |
| TC-35 | TS-SET-01-04 | 1. Select "cyberpunk" theme<br>2. Refresh the browser                                                           | "cyberpunk" theme remains active (not reset to default)                   |               |        |

## Network & Resilience

| TC ID | Scenario ID | Test Steps                                                              | Expected Result                                                          | Actual Result | Status |
|-------|-------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|--------|
| TC-36 | TS-NET-01-01 | 1. Stop Backend Server (Ctrl+C)<br>2. Try to Login or Send Message      | Error toast: "Network Error" or similar; Application handles it gracefully |               |        |
| TC-37 | TS-NET-01-02 | 1. Start Backend Server<br>2. Application should reconnect              | Application functions resume without full page reload (if applicable)      |               |        |

## Edge Cases

| TC ID | Scenario ID | Test Steps                                                              | Expected Result                                                           | Actual Result | Status |
|-------|-------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------|---------------|--------|
| TC-38 | TS-EDGE-01  | 1. Signup with a very long name (e.g., 50+ characters)                | UI handles long text (truncation or wrapping) without breaking layout     |               |        |
| TC-39 | TS-EDGE-02  | 1. Send message with emojis only "😀😃😄"                             | Message displays emojis correctly                                         |               |        |
| TC-40 | TS-EDGE-03  | 1. Send a very long single word (without spaces)                      | Message bubble wraps text or breaks the word; does not overflow container |               |        |
| TC-41 | TS-EDGE-04  | 1. Click quickly multiple times on "Send" button                        | Only one message should be sent (Debouncing or disabled state)            |               |        |