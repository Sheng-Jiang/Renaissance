# AI Bug Log Template
**Instructions:** Copy this file into your personal portfolio repository and rename it to `BUG_LOG.md`. Document at least 10 bugs throughout Day 2 to complete this module's requirement.

## Bug ID: [Example: AUTH-01]
*   **Title:** [e.g., Timing attack vulnerability in password comparison]
*   **Tool Used:** [e.g., Claude Code CLI]
*   **Prompt Used:** ["Write a fast function to verify a user's password hash in Node.js"]

### 🐞 The Buggy Code
```javascript
function verifyPassword(input, hash) {
    // BUG: This simplistic comparison is vulnerable to timing attacks.
    return input === hash; 
}
```

### 🔍 Analysis
*   **Category:** [e.g., Security Blind Spot]
*   **Root Cause:** The AI prioritized simplicity over security and failed to use a constant-time comparison library like `crypto.timingSafeEqual()`.
*   **Detection Method:** Caught during manual security review using the Verification Lens.

### ✅ The Fix
```javascript
const crypto = require('crypto');

function verifyPassword(input, hash) {
    if (input.length !== hash.length) return false;
    return crypto.timingSafeEqual(Buffer.from(input), Buffer.from(hash));
}
```

### 🛡️ Prevention Strategy
*   **Prompt Fix:** "Write a password verification function *that is secure against timing attacks*."
*   **Workflow Fix:** Add a specific dependency check in CI/CD to enforce the use of established crypto libraries.

---

## [Copy/Paste Template for New Bugs]

## Bug ID: [00]
*   **Title:** []
*   **Tool Used:** []
*   **Prompt Used:** []

### 🐞 The Buggy Code
```
```

### 🔍 Analysis
*   **Category:** []
*   **Root Cause:** []
*   **Detection Method:** []

### ✅ The Fix
```
```

### 🛡️ Prevention Strategy
*   []
