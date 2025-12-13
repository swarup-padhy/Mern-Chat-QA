# [BUG-05] Content Overflow & Layout Breakage

## Issue Summary
**ID**: BUG-05
**Title**: UI layout breaks with long text inputs (Names/Messages)
**Severity**: Minor
**Status**: Open

## Description
The application's user interface does not correctly handle extreme text inputs, specifically very long usernames or long single words without spaces in chat messages. This results in visual components breaking, overlapping, or extending beyond their containers.

## Steps to Reproduce
**Scenario A (Long Name)**:
1.  Navigate to Signup.
2.  Create a user with a 50+ character name.
3.  Login and observe the display of the name in the Profile/Sidebar/Header.

**Scenario B (Long Word)**:
1.  Open a chat window.
2.  Send a message consisting of a single continuous string of 50+ characters (e.g., "aaaaaaaa...").

## Expected Result
-   **Long Name**: Name should be truncated with ellipses (...) or wrapped gracefully.
-   **Long Word**: Text should break to the next line or be hidden with overflow handling; the chat bubble should not exceed the container width.

## Actual Result
-   **Long Name**: Layout breaks; text pushes other elements out of alignment.
-   **Long Word**: Text overflows the chat bubble and potentially the chat window container.

## Environment
-   **URL**: `http://localhost:5173`
-   **Browser**: Chrome v120
-   **OS**: Windows 11
