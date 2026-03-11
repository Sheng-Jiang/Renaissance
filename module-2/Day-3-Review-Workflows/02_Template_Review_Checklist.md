# Template: AI Code Review Checklist

**Instructions:** Copy this checklist into your repository. You will use this to evaluate the Pull Requests in today's lab, and it will become your standard PR template.

## 1. Intent Verification
*   [ ] Does the code solve the specific problem described in the issue/spec?
*   [ ] Did the AI make any unstated assumptions about the business logic?
*   [ ] Is the implementation appropriate for the domain?

## 2. Correctness & Edge Cases
*   [ ] Is the happy path correct?
*   [ ] Are error paths explicitly handled (nulls, undefined, empty lists, boundary values)?
*   [ ] Are there potential race conditions or concurrency issues?

## 3. Security Scan
*   [ ] Is user input sanitized and validated?
*   [ ] Is output encoded properly?
*   [ ] Are authentication/authorization checks present where needed?
*   [ ] Are there any leaked or hardcoded secrets?

## 4. Performance & Scalability
*   [ ] What is the time/space complexity? Is it optimal?
*   [ ] Are there excessive database queries (N+1 query problem)?
*   [ ] Would this code perform reasonably under a 10x traffic spike?

## 5. Maintainability & Standards
*   [ ] Does the code follow our team's naming conventions and structural patterns?
*   [ ] Or does it look like generic, context-less AI copy-paste?
*   [ ] Could a new team member understand this without AI assistance?

## 6. Test Quality
*   [ ] Do the tests actually verify behavior (or do they just blindly assert what the code returns)?
*   [ ] Are the edge cases identified in Section 2 covered by tests?
*   [ ] Are the tests deterministic and fast?
