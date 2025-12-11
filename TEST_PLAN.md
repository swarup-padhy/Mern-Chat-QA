# Test Plan: Chat App RC1

### 1. The Strategy
We act like real users. We assume the network is flaky, the users are impatient, and the inputs are messy.

### 2. What We Test (Scope)
- **Auth**: Can I get in? Can I get out? Do you stop me if I'm fake?
- **Chat**: Is it fast? Does it break if I send an image? Do you see what I type?
- **Resilience**: If I kill the server, does the app freak out or just wait patiently?

### 3. The Environment
- **Localhost**: Where the magic happens first.
- **Network Throttling**: Because 5G isn't everywhere. Tested on "Slow 3G" simulation.

### 4. Pass/Fail Criteria
- **PASS**: The feature works, looks good, and doesn't throw console errors.
- **FAIL**: Crash, data loss, or "Undefined is not a function".

### 5. Execution
See `02_TEST_CASES.md` for the run logs.
