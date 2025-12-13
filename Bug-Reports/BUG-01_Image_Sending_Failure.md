# [BUG-01] Image Sending Failure & UI Block

## Issue Summary
**ID**: BUG-01
**Title**: Image sending fails and causes the application to become unresponsive
**Severity**: Critical
**Status**: Open

## Description
When attempting to send an image attachment in a chat, the message fails to send. Additionally, after the failed attempt, the "Send" button becomes unresponsive for all subsequent text or image messages across any selected user. The application requires a full page refresh to restore functionality.

## Steps to Reproduce
1.  Login to the application.
2.  Select any user from the sidebar to open a chat.
3.  Click the **Image Attachment** icon.
4.  Select a valid image file (e.g., `.jpg` or `.png`).
5.  Click the **Send** button.
6.  Attempt to send a text message to the same or different user.

## Expected Result
-   The image should be sent and appear in the chat window.
-   The input field should clear and allow further messaging.

## Actual Result
-   The image is not sent.
-   The UI remains in a "sending" state or ignores further "Send" clicks.
-   Messaging functionality is blocked globally until refresh.

## Environment
-   **URL**: `http://localhost:5173`
-   **Browser**: Chrome V142.0.7444.176
-   **OS**: Windows 11
