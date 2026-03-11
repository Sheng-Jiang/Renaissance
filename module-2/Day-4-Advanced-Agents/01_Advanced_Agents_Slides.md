---
marp: true
theme: default
paginate: true
---

![bg right:60% fit](cover.png)
# Module 2: AI-Augmented Development
## Verification, Governance & the Quality Gate
**Day 4: Advanced Agent Development**

---

# Agent Architecture Patterns
Recap: A basic agent loops `Message -> Agent -> LLM -> Tools -> Response`.

**Today's Architectural Enhancements:**
1.  **Multi-Tool Agents:** Granting the agent varied, specialized tools to invoke contextually.
2.  **Memory-Augmented Agents:** Persistent states that allow the agent to evolve across conversations.
3.  **Integration Agents:** Connecting to external services (e.g., GitHub, databases, external APIs).

*Security Note: Every new tool and integration is a new attack surface.*

---

# The Tool Selection Problem
How does an agent decide which tool to use?

*   It heavily relies on **System Prompt Guidance**.
*   It requires extremely precise **Function Descriptions**.
*   It utilizes robust **Tool Routing logic**.

If your tool descriptions are vague, the LLM will hallucinate arguments or pick the wrong tool entirely.

---

# Memory Architectures
Moving from flat conversation logs to structured knowledge.

*   **Short-term Memory:** Current conversation context (the chat history matrix).
*   **Long-term Memory:** Persistent facts, user preferences, and project states. (In Nanobot, this is achieved via Markdown files).
*   **Episodic Memory:** Key events and architectural decisions made over time.

---

# Today's Sprints

You will spend today extending your Nanobot fork from Module 1.

1.  **Build Sprint 1 (Multi-Tool):** Add at least 3 tools to your agent, including a mandatory GitHub API integration.
2.  **Build Sprint 2 (Memory System):** Implement structured, file-based memory (user profiles, running projects, corrections list).
3.  **Integration & Showcase:** Wire it all together, test it, and demo your advanced agent to a peer for a live code review.
