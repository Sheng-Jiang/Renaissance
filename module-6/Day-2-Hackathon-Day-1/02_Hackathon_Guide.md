# Hackathon Rules & Best Practices Guide

## The Setup Checklist (First 2 Hours)
Before anyone writes a line of feature code, ensure your team has completed this checklist:

*   [ ] Repository created and shared with all team members.
*   [ ] GitHub Projects board populated with the Task Breakdown from Day 1.
*   [ ] CI/CD Pipeline configured (compiles code and runs a basic "Hello World" test).
*   [ ] Development environment standard agreed upon (e.g., Node version, Python version, Docker compose file).
*   [ ] ClawSwarm or multi-agent configuration initialized and connected.

## How to Manage Scope
During a 48-hour sprint, scope creep is lethal. Use the **MoSCoW Method** for every feature request that pops up during the build:

*   **Must Have:** If we don't have this, the MVP doesn't solve the core problem. (Do this now).
*   **Should Have:** Important, but we can fake it if we run out of time.
*   **Could Have:** Nice to have. Put it in the icebox.
*   **Won't Have:** Explicitly out of scope for this hackathon.

## Collaboration Rules
*   **Branching:** Do not work directly on `main`. Prefix branches with your name and feature (e.g., `sheng/auth-stub`).
*   **Merging:** PRs should be small. A massive 800-line PR will halt your team's velocity because nobody will want to review it.
*   **Communication:** Keep an open channel (huddle, discord, zoom) even if you aren't talking. Presence matters.

## When to Ask for Help
Do not spend more than **30 minutes** stuck on a configuration error. If Claude Code, Copilot, or ClawSwarm can't fix it in 30 minutes, flag an instructor immediately. Your time is too valuable to spend debugging Webpack configurations.
