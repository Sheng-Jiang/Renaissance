---
marp: true
theme: default
paginate: true
---

# Module 8: Communication, Leadership & Enterprise Scale
## Day 4: Technical Writing & Enterprise ADRs
**Renaissance Developer Academy**

---

# Two Documents, One Truth

Today you write **two documents** about the same project:

1.  **A Technical Specification** — for engineers to build from.
2.  **An Executive Summary** — for leaders to fund it.

If you can do both well, you can bridge any audience gap.

---

# Technical Specification Anatomy

| Section | Purpose |
|---|---|
| Problem Statement | Grounded in evidence |
| Goals & Non-Goals | Explicitly scope what you will/won't build |
| Technical Design | Architecture, data models, API contracts |
| Alternatives Considered | ≥ 2 alternatives with trade-off analysis |
| Security Considerations | Reference OWASP or your Day 3 audit |
| Testing Strategy | How you'll verify correctness |
| Rollout Plan | How you'll deploy safely |

---

# Executive Summary Anatomy

Use the **Minto Pyramid**: Situation → Complication → Resolution.

Rules:
*   **Lead with the recommendation:** "We should invest $X in Y to achieve Z."
*   **No architecture diagrams.** No code. No unexplained acronyms.
*   **Include:** business impact (quantified), timeline, cost, top risk.
*   **The test:** Could a non-technical VP make a funding decision from this alone?

---

# Today's Sprints

1.  **Write** a technical specification (for OpenClaw improvement or your capstone).
2.  **Write** a 1-page executive summary of the same project.
3.  **Peer cross-check:** Does the tech spec match the exec summary?
4.  **Enterprise ADR:** Write an ADR for a significant architectural decision.
