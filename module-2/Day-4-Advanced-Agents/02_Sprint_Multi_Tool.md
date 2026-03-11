# Build Sprint: Multi-Tool Agent
**Time: 90 Minutes**

## Overview
Extend your Nanobot fork from Module 1 by implementing a multi-tool architecture.

## Instructions
Your goal is to ensure your agent has access to at least 3 distinct tools.

### Tool 1: Existing Custom Skill
Ensure the custom skill you built in Module 1 is fully functional and refactored if necessary.

### Tool 2: GitHub Integration (Mandatory)
Build a tool that interfaces with the GitHub API (or the `gh` CLI). 
*   **Capabilities:** Query open issues, create issues, and list recent commits.

### Tool 3: Integrator's Choice
Choose one of the following to build:
*   **Option A: Web Search Tool** (Use a search API or basic web scraping).
*   **Option B: File Analysis Tool** (Read and summarize local documents).
*   **Option C: Code Analysis Tool** (Run linters or static analysis and report back).
*   **Option D: Calendar/Scheduling Tool** (Integrate with a calendar API).

## Verification Check
Test each tool *independently* before integrating it into the agent's main system prompt. Ensure the function descriptions you provide to the LLM are hyper-specific so the agent routes commands correctly.
