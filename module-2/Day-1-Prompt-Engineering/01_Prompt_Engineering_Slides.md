---
marp: true
theme: default
paginate: true
---

![bg right:60% fit](cover.png)
# Module 2: AI-Augmented Development
## Verification, Governance & the Quality Gate
**Day 1: Advanced Prompt Engineering & AI Code Generation**

---

# The AI Multiplier Model (Recap)

1.  **AI Generation Engine:** Speed & Scope
2.  **Human Quality Gate:** Verification & Architecture
3.  **Business Value:** Reliability & Delivery

*The focus of Module 2 is entirely on the Quality Gate.*

---

# Why Prompt Structure Matters

Code generation is easy. Generating **verifiable code** is hard. 

*   Predictable inputs $\rightarrow$ verifiable outputs $\rightarrow$ repeatable quality.
*   Sloppy prompts create unverifiable code.

---

# The 5 Layers of a Structured Prompt
The Anatomy of an Effective Prompt:

1.  **Context:** Project background, stack, coding standards.
2.  **Task:** Specific, bounded request with acceptance criteria.
3.  **Constraints:** Language, framework, security, performance.
4.  **Output Format:** File structure, naming, documentation expectations.
5.  **Verification Hooks:** Ask the AI to explain its reasoning, flag uncertainty, suggest tests.

---

# Beyond Single-Shot Prompts

As complexity scales, a single prompt breaks down.

1.  **Chain-of-Thought Prompting:** Asking the AI to reason *before* coding.
    *   *Example:* "Analyze requirements, identify 3 approaches with trade-offs. Then implement the best one."
2.  **Decomposition Prompting:** Breaking a task into verifiable subtasks.
    *   *Example:* Instead of "Build auth," prompt for: 1) Data model 2) Hashing 3) Endpoints 4) Tests. 
    *   *Why?* Each step is independently verifiable.

---

# Today's Labs

1.  **Prompt Playbook:** Build 5 systematic patterns (Scaffolding, Test Generation, Refactoring, Debugging, Documentation).
2.  **Comparative Lab:** Rebuild a feature using single-shot vs. chain-of-thought vs. decomposition.
3.  **Prompt Portability Test:** Test your best prompts across Claude, Kiro, and Antigravity.
4.  **Peer Review:** Exchange playbooks and test their resilience.
