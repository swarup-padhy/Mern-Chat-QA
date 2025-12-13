# [BUG-02] Profile Picture Update Failure

## Issue Summary
**ID**: BUG-02
**Title**: Profile picture update fails silently
**Severity**: Major
**Status**: Open

## Description
Users are unable to update their profile profile picture. When selecting a new image to upload, the action completes without any error message, but the profile picture remains unchanged.

## Steps to Reproduce
1.  Login to the application.
2.  Navigate to the **Profile** page.
3.  Click the **Edit** icon on the current avatar.
4.  Select a new image file from the local machine.
5.  Wait for the upload process to complete.

## Expected Result
-   A success notification (e.g., "Profile updated") should appear.
-   The new image should immediately replace the old avatar on the Profile page and Sidebar.

## Actual Result
-   No success or error message is displayed.
-   The avatar image reverts to or stays as the previous image.

## Environment
-   **URL**: `http://localhost:5173`
-   **Browser**: Chrome
-   **OS**: Windows 11
