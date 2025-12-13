# [BUG-03] User List Fails to Update in Real-Time

## Issue Summary
**ID**: BUG-03
**Title**: Sidebar user list does not include new users until refresh
**Severity**: Major
**Status**: Open

## Description
When a new user registers an account, other currently logged-in users do not see this new user appear in their sidebar list in real-time. The list is only updated after manually refreshing the browser.

## Steps to Reproduce
1.  Login as **User A** in Browser Window 1.
2.  Open a new Incognito/Private window (Browser Window 2).
3.  Navigate to the Signup page and create a new account for **User B**.
4.  After User B attempts to sign up, observe the sidebar in **User A's** window.

## Expected Result
-   **User B** should appear in **User A's** sidebar list automatically without intervention.

## Actual Result
-   **User B** is missing from **User A's** list.
-   User A must press `F5` or Reload the page to see User B.

## Environment
-   **URL**: `http://localhost:5173`
-   **Browser**: Chrome (Testing cross-window sync)
-   **OS**: Windows 11
