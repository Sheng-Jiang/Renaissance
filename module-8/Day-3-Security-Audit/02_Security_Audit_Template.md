# Exercise: Security Audit Report Template
**Time: Full Day**

## Phase 1: Threat Model (45 mins)
1. **Assets:** List the 5 most critical assets in OpenClaw (user data, API keys, agent memory, skill code, system config).
2. **Threat Actors:** Identify the 3 most likely attackers and their motivations.
3. **Attack Surface Map:** Use STRIDE to identify entry points for each threat type.

## Phase 2: Vulnerability Assessment (90 mins)
For each attack surface, attempt to identify specific vulnerabilities:

| Category | What to Test |
|---|---|
| **Prompt Injection** | Craft inputs that override agent system prompts |
| **Skill Security** | Review ClawHub installation flow for supply chain risks |
| **Container Isolation** | Review Docker config for escape vectors |
| **Data Leakage** | Check logging and monitoring for sensitive data exposure |
| **API Security** | Review authentication and authorization |

## Phase 3: Risk Scoring (45 mins)
Score each finding using the matrix:

| | Unlikely | Possible | Likely | Certain |
|---|---|---|---|---|
| **Critical** | Medium | High | Critical | Critical |
| **High** | Low | Medium | High | Critical |
| **Medium** | Low | Low | Medium | High |
| **Low** | Info | Low | Low | Medium |

## Phase 4: Write the Report (90 mins)
Use this structure:

### Executive Summary
One paragraph: overall posture, critical findings count, recommendation.

### Methodology
What you tested, tools used, what was out of scope.

### Findings Table
| # | Severity | Finding | Recommendation |
|---|---|---|---|
| 1 | Critical | [Description] | [Fix] |
| 2 | High | [Description] | [Fix] |

### Detailed Findings (Top 3)
For each:
- Description of the vulnerability
- Steps to reproduce
- Business impact if exploited
- Recommended fix with implementation guidance
- Priority and estimated effort

### Recommendations Summary
Prioritized list of security improvements.
