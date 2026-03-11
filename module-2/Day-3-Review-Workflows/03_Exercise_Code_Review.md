# Exercise: AI-Aware Code Review Practice
**Time: 75 Minutes**

## Overview
You will practice applying your newly created `AI Code Review Checklist` to realistic, AI-generated Pull Requests.

## Instructions
Your instructor will provide 4 links to Pull Requests containing AI-generated code for various features.
*   **PR #1:** A user registration flow with email verification (Python/Flask)
*   **PR #2:** A dashboard API with filtering and pagination (Node/Express)
*   **PR #3:** A file processing pipeline with error handling (Python)
*   **PR #4:** A WebSocket real-time notification system (TypeScript)

### Part 1: Review (60 mins)
Choose 2 of the 4 PRs. Evaluate them strictly using your checklist.

For each PR, leave **structured review comments on GitHub**:
1.  **[Approve]** At least 1 comment explaining what's good and why it's correct.
2.  **[Request Changes]** At least 1 comment with specific, actionable feedback on a bug or anti-pattern.
3.  **[Question]** At least 1 comment probing the AI's assumptions or unstated intent.

*(Note: "LGTM" or pure nitpicking on style without addressing logic/intent is not acceptable).*

### Part 2: Calibration (15 mins)
Find another student who reviewed the same PRs. Compare your findings.
*   Did your checklist catch real issues?
*   Where did it miss? Update your checklist based on this calibration.
