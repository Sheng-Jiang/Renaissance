---
marp: true
theme: default
paginate: true
---

# Module 8: Communication, Leadership & Enterprise Scale
## Day 3: Security Audit Lab
**Renaissance Developer Academy**

---

# Security Is Not Just the Security Team's Job

Every technical leader must be able to:
1.  **Evaluate** the security posture of a system.
2.  **Identify** vulnerabilities using structured methodology.
3.  **Communicate** findings to both engineers and executives.
4.  **Prioritize** remediations based on risk.

---

# Security Audit Methodology

**Threat Modeling:**
- Assets: What's worth protecting? (User data, API keys, agent memory)
- Threat Actors: Who would attack? (Malicious user, compromised plugin, insider)
- Attack Surfaces: Where are the entry points?

**STRIDE Framework:**
| Threat | Question |
|---|---|
| **S**poofing | Can someone pretend to be someone else? |
| **T**ampering | Can data be modified without detection? |
| **R**epudiation | Can actions be denied without proof? |
| **I**nformation Disclosure | Can sensitive data leak? |
| **D**enial of Service | Can the system be overwhelmed? |
| **E**levation of Privilege | Can a user gain unauthorized access? |

---

# OWASP Top 10 for LLM Applications

Key risks for AI-powered systems like OpenClaw:
1.  **Prompt Injection:** Crafted inputs that override agent behavior.
2.  **Insecure Output Handling:** Agent outputs that aren't sanitized.
3.  **Supply Chain Vulnerabilities:** Compromised skills from ClawHub.
4.  **Model DoS:** Requests designed to exhaust compute resources.

---

# Today's Sprints

1.  **Threat Model** the OpenClaw system (assets, actors, surfaces).
2.  **Vulnerability Assessment:** Attempt to find real issues.
3.  **Write** a professional security audit report with findings and recommendations.
