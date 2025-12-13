# [BUG-02] Profile Picture Update Failure

## Issue Summary
**ID**: BUG-02
**Title**: Profile picture update fails silently
**Severity**: Major
**Status**: Open

## Description
Users are unable to update their profile picture. The functionality fails with an explicit error toast, and the profile picture remains unchanged.

## Steps to Reproduce
1.  Login to the application.
2.  Navigate to the **Profile** page via the settings menu.
3.  Click the **Camera/Edit** icon on the current avatar.
4.  Select a new image file from the local machine.
5.  Observe the UI feedback.

## Expected Result
-   A success notification (e.g., "Profile updated") should appear.
-   The new image should immediately replace the old avatar on the Profile page and Sidebar.

## Actual Result
-   An "Internal Server Error" toast appears.
-   The avatar image does not change.

## Environment
-   **URL**: `http://localhost:5173/profile`
-   **Browser**: Chrome v120
-   **OS**: Windows 11
