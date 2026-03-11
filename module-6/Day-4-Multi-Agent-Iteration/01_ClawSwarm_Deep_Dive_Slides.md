---
marp: true
theme: default
paginate: true
---

![bg right:60% fit](cover.png)
# Module 6: Rapid Prototyping & Design Sprints
## Day 4: Multi-Agent Iteration
**Renaissance Developer Academy**

---

# The Feature Freeze

At 11:00 AM today, we enforce a strict feature freeze.
You will stop adding new capabilities. You will start polishing what exists.

*Why?*
Because a perfect, smooth 3-step MVP looks significantly better in a demo than a clunky, broken 10-step behemoth.

---

# ClawSwarm: Orchestrated Multi-Agent Builds

While your team polishes the frontend, let's look at how Multi-Agent orchestration actually works under the hood.

1.  **The Planner Agent (Opus/Pro):** Breaks down the goal into a DAG (Directed Acyclic Graph) of tasks.
2.  **The Coder Agent (Sonnet/Flash):** Executes individual file modifications.
3.  **The Reviewer Agent:** Triggers the build tool and linting, bouncing errors back to the Coder.

Where do Humans fit in? *We set the goals and we define the boundaries.*

---

# Shared Memory Contexts

A major bottleneck of single LLMs is context limits. Multi-agent systems use shared files as "blackboards."

*   `GOALS.md`
*   `DECISIONS.md`
*   `PROJECT_STATUS.md`

By having agents read and write to these centralized files, the system maintains state across hundreds of individual API calls.

---

# Today's Sprints

1.  **The Fix Sprint:** Implement the "Fix Now" and "Fix Tomorrow" items from your User Testing backlog.
2.  **The ClawSwarm Lab:** Individually spin up a 2-agent ClawSwarm cluster and test cross-agent communication.
3.  **Feature Freeze & Polish:** At 11:00, stop building. Start writing documentation, `README` files, and architecture diagrams.
4.  **Demo Rehearsals:** Run your 10-minute demo start to finish with a stopwatch. Do it twice.
