# [BUG-04] Network Error Handling & Reconnection Failure

## Issue Summary
**ID**: BUG-04
**Title**: Missing offline notification and failure to auto-reconnect
**Severity**: Major
**Status**: Open

## Description
The application fails to gracefully handle network interruptions or backend server downtime. When the backend is unreachable, the user receives no feedback (no "Network Error" toast). Furthermore, when the connection is restored, the application does not automatically reconnect; the user must manually refresh the page to resume chat functionality.

## Steps to Reproduce
1.  Login to the application.
2.  Simulate a network failure or manually stop the backend server.
3.  Attempt to send a message or navigate.
4.  Restaurant the network/backend server.
5.  Observe the application status.

## Expected Result
-   **Offline**: A visible toast or banner should inform the user of the connection loss.
-   **Recovery**: The application should detect the restored connection and auto-reconnect the socket/session without a full page reload.

## Actual Result
-   **Offline**: No error message appears; the UI generally fails silently.
-   **Recovery**: The application remains in a disconnected state indefinitely until the page is refreshed.

## Environment
-   **URL**: `http://localhost:5173`
-   **Browser**: Chrome v120
-   **OS**: Windows 11
